# Write-up Template

  

### Analyze, choose, and justify the appropriate resource option for deploying the app.

  

*For **both** a VM or App Service solution for the CMS app:*

- *Analyze costs, scalability, availability, and workflow*

  

## Azure App Service

  

### cost
- the cost in app service is depends on th os you choose and the time of creation and the features you want e.g auto-scale

- there is different pricing levels, the price level determines the app service features

- for the Basic pricing level and Linux OS the price will be $0.018/hour[1]

  

### scalability
- supprt auto scaling

- you can scale up or out, for scaling up you have a limit that you can not exceed [2]

  

### availability
- App service can be configured to be zone redundent and the the VM instances will be spreaded to three zones inside the region [3]

--The limitaton on app service availablity

- Requires Premium v2 or Premium v3 App Service plans.

- Minimum instance count of three is enforced.

- Availability zones can only be specified when creating a new App Service plan. A pre-existing App Service plan can't be converted to use availability zones

- it's only limited on a small number of reagions

  

--------------------

  

## Azure Virtual Machine

### cost

- The cost depends on the resources, for b1s instance the cost is *$7.5920/month*[4]

### scalability

- scale set can be created and it can be increased or decreased based on the resource demand defined schedule [5]

### availability

- we can use virtual machine scale set for high-availability[5]

  -----
  

- *Choose the appropriate solution (VM or App Service) for deploying the app*

**I think in this app the appropriate solution is azure app service**

- *Justify your choice*

  

-- I choosed app service because a set of things which is :

- Tha app is small and it dose not required a lot of power

- In terms of managment, in such app we do not need a full access to the underlaying machine

- The app service fuflfill the need of the app with much cheaper price

- App service already supporting the same stack that we built the app with (python)

### Assess app changes that would change your decision.

- If the app need to expand or shrink frequently mostly i will go with Azure VM because it provides resiliency, also if the app requires high-availability

- If i need to access

- It worth to mention also that app service does not support a wide range of tech stacks so usually if i'm using a stack that is not supported by app services i will go with Azure VM

  

*Detail how the app and any other needs would have to change for you to change your decision in the last section.*

  
  

## Resources

[1]https://azure.microsoft.com/en-us/pricing/details/app-service/windows/

[2]https://learn.microsoft.com/en-us/azure/app-service/manage-scale-up

[3]https://learn.microsoft.com/en-us/azure/availability-zones/migrate-app-service

[4]https://azure.microsoft.com/en-us/pricing/details/virtual-machines/windows/

[5]https://learn.microsoft.com/en-us/azure/virtual-machine-scale-sets/overview