# Networks

[toc]

## Troubleshooting

Steps in making HTTP calls.

1. DNS resolution. Connecting to a DNS server to obtain the IP address of the server.
2. TCP handshake. The client initiates a synchronization request, the server acknowledges this and the client comfirms the acknowledgement.
3. TLS handshake. See [security](security.md).
4. HTTP requests and responses.

The server handles authorization, sessions and caching.



### Tools

See this [connecitivity](https://github.com/voschezang/mash/blob/main/src/mash/webtools/verify_server.py) script and this [load test](https://github.com/voschezang/mash/blob/main/src/mash/webtools/parallel.py) script.



## OSI Model

[7 Layers](https://en.wikipedia.org/wiki/OSI_model#Layer_architecture)

<table>
  <caption>OSI model</caption>
<tbody>
  <tr>
    <th colspan="3">Layer</th>
  <th>Protocol data unit (PDU)</th>
  <th>Function</th>
  </tr>
<tr>
<th rowspan="4">Host<br />layers</th>
<td style="background:#d8ec9b;">7</td>
<td style="background:#d8ec9b;">Application</td>
<td style="background:#d8ec9c;" rowspan="3">Data (`100011011`)</td>
<td style="background:#d8ec9c;">High-level APIs, including resource sharing, remote file access</td></tr>
<tr>
<td style="background:#d8ec9b;">6</td>
<td style="background:#d8ec9b;">Presentation</td>
<td style="background:#d8ec9b;">Translation of data between a networking service and an application; including encoding, encryption, compression</td></tr>
<tr>
<td style="background:#d8ec9b;">5</td>
<td style="background:#d8ec9b;">Session</td>
<td style="background:#d8ec9b;">Managing communication sessions, i.e., continuous exchange of information in the form of multiple back-and-forth transmissions between two nodes
</td></tr>
<tr>
<td style="background:#e7ed9c;">4</td>
<td style="background:#e7ed9c;">Transport</td>
<td style="background:#e7ed9c;">Segmentation, Datagram</td>
<td style="background:#e7ed9c;">Reliable transmission of data segments between points on a network, including segmentation, acknowledgement, multiplexing. E.g. TCP, UDP</td></tr>
<tr>
<th rowspan="3">Media<br />layers</th>
<td style="background:#eddc9c;">3</td>
<td style="background:#eddc9c;">Network</td>
<td style="background:#eddc9c;">Packet</td>
<td style="background:#eddc9c;">Structuring and managing a multi-node network, including adressing, routing and network traffic control. E.g. IP</td></tr>
<tr>
<td style="background:#e9c189;">2</td>
<td style="background:#e9c189;">Data link</td>
<td style="background:#e9c189;">Frame</td>
<td style="background:#e9c189;">First abstraction above physical layer. E.g. ethernet</td></tr>
<tr>
<td style="background:#e9988a;">1</td>
<td style="background:#e9988a;">Physical</td>
<td style="background:#e9988a;">Bit, Symbol
</td>
<td style="background:#e9988a;">Convert bits to a time-depenent signal (a stream)</td>
</tr>
</tbody>
</table>
**Alternative Models**

[src](https://en.wikipedia.org/wiki/Internet_protocol_suite#Layer_names_and_number_of_layers_in_the_literature)

<table>
<thead><tr><th>OSI Layer</th><th>5-Layer</th><th>3-Layer</th></tr></thead>
<tbody>
  <tr>
    <td>Application</td>
    <td rowspan="3">Application</td>
    <td rowspan="3">Application / Transport</td>
  </tr>
  <tr><td>Presentation</td></tr>
  <tr><td>Session</td></tr>
  <tr>
    <td>Transport</td>
    <td>Transport</td>
    <td rowspan="2">Host-to-host</td>
  </tr>
  <tr>
    <td>Network</td>
    <td>Internet</td>
  </tr>
  <tr>
    <td>Data Link</td>
    <td>Network Access / Data Link</td>
    <td>Network Interface</td>
  </tr>
  <tr>
    <td>Physical<br></td>
    <td>Physical</td>
    <td></td>
  </tr>
</tbody>
</table>


