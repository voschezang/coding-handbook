# Organization Scale

Scaling up an organization while maintaining centralized control is inherently difficult. Factors such as autonomy, alignment, control and efficiency may work against each other.



Organizations may grow and adapt. There are a few phases that can be distinguished:

![scale-up-out](../img/scale-up-out.png)

Each component has a *bounded context*. This is an internal, local model. These may include

- A **core** domain. The components that make this organization unique. These <u>provide</u> value.
- **Platforms**. These are generic components that are vital for the functioning of the core domain. These <u>enable</u> value.
- **Contextual** or supporting domains. E.g. interfaces in hexagonal architecture.





**Scaling Agile**

> Agile transformations are done by removing obstacles, rather than by enforcing change.

Achieving high agility of small teams is much simpler that doing it for multiple teams. A few guidelines to do this:

- Scale down. Focus on the core business and outsource the rest.
- Scale out. Divide an organization into independent, autonomous components.
- Scale in. Increase alignment without impeding autonomy. E.g. create a shared vision.



**In IT organizations**

At certain scales, the structure incentivizes **local** optimizations due to the inherent difficulty of making changes that affect other components.

- In functional teams this could lead to strict SLAs and slow handovers.
- In feature teams this can lead to diverging features. This increases duplication.



## Product Scale

See [product increments](../labour/increments.md).

![product-scaling](../img/product-scaling.png)