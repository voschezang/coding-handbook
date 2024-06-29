# Statistics

Statistical models. Regression and classification.

[toc]

## Model Performance



### Bias-variance tradeoff

There is no [free lunch](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff); making models specific to one dataset decreases the performance on all others (i.e. generalization).

Models are exclusive by nature. They are biassed to a given scenario and context.



### Class Imbalance

In classification, data may not be distributed equally. E.g. a model that classifies any patient as healthy is useless, but it will still have a high accuracy for rare disseases.

Alternative metrics are [precision and recall](https://en.wikipedia.org/wiki/Precision_and_recall). Model performance can be tuned towards specifc metrics, based on its intended application.

| Metric               | Targets                        |
| -------------------- | ------------------------------ |
| Accuracy             | Correctness of predictions     |
| Precision            | Relevancy of findings          |
| Recall (sensitivity) | Ability to find relevant items |

A [confusion matrix](https://en.wikipedia.org/wiki/Confusion_matrix) can be used to summarize the performance.

<table><tbody>
<tr>
  <td rowspan="2" style="border:none;"></td>
  <td style="border:none;"></td>
  <td colspan="2"><b>Prediction</b></td>
</tr>
<tr>
  <td><b>Total population: P + N</b></td>
  <td><b>Positive</b></td>
  <td><b>Negative</b></td>
</tr>
<tr>
  <td rowspan="2"><b>Reality</b></td>
  <td><b>Positive (P)</b></td>
  <td>True positive (TP)</td>
  <td>False negative  (FN)</td>
</tr>
<tr>
  <td><b>Negative (N)</b></td>
  <td>False positive (FP)</td>
  <td>True negative (TN)</td>
</tr>
</tbody></table>
