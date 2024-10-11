# Scenario 1 - Monitoring and Recovery

## Overview

In this scenario, attendees will be split into a series of teams of 4-5 people. Each team should be multi-skilled with attendees from either infrastructure, AppDev or Data skills to complement each other during the event. Teams will be given an identical working environment based on a version of the Contoso Traders ECommerce application. The teams will be responsible for understanding, based on an architecture diagram and access to the Azure environment, the application itself, then configuring any monitoring they feel is necessary. During this time, the coaches will assume the role of the developers of the application and can answer questions from the teams to help them gain a better understanding of the application.
Coaches will then run a series of chaos experiments simultaneously against all environments. One experiment at a time will be run and each team will be scored, based on how well they react to the chaos that is happening. The experiments will build in complexity during the day.

## Objectives

- Simulate a real world scenario where the documentation for an application may be out of date 
- Understand how to monitor an application and react under time pressure

## Deploy the Game Day environment

For this game day, we have one deployment of the application per team. Follow the [deployment guide for scenario 1](deploy-scenario-1.md). There will be one resource group per team (denoted by the digit at the end of the DEPLOYMENT_NAME prefix e.g. chaos1) and one resource group for the coaches (denoted by a c at the end of the DEPLOYMENT_NAME prefix e.g. chaosc). You should ensure that each team only have contributor permissions to their two resource groups, e.g. chaos1-rg and chaos1-aks-rg. This prevents teams from accidentally, or purposefully, affecting other team's environments The coaches should have permissions on all resource groups in the environment.

## Flow of the Hackathon

> **Note**: The timings are purposefully tight to increase the pressure on the teams

### 0900
- **15 mins**: Kick off by lead coach
- **30 mins**: Start by giving teams the architecture diagram and access to the resource group

### 0945
- **15 mins**: Coach overview of Health Modelling
- **30 mins**: Failure mode analysis of the application

### 1030
- **15 mins**: Coach overview of monitoring
- **30 mins**: Create monitoring dashboards and alerts

### 1115
- **30 mins**: Chaos experiment 1
- **15 mins**: Discuss what happened, who picked up the issue, how?
- **10 mins**: Coach overview of what you should have found

### 1210
- **Lunch**

### 1310
- **30 mins**: Chaos experiment 2
- **15 mins**: Discuss what happened, who picked up the issue, how?
- **10 mins**: Coach overview of what you should have found

### 1405
- **30 mins**: Chaos experiment 3
- **15 mins**: Discuss what happened, who picked up the issue, how?
- **10 mins**: Coach overview of what you should have found

### 1500
- **30 mins**: Chaos experiment 4
- **15 mins**: Discuss what happened, who picked up the issue, how?
- **10 mins**: Coach overview of what you should have found

### 1555
- **30 mins**: Chaos experiment 5
- **15 mins**: Discuss what happened, who picked up the issue, how?
- **10 mins**: Coach overview of what you should have found

### 1650
- **45 mins**: Coach overview of chaos engineering and demo of chaos studio

### 1735
- **Wrap up**

### 1745
- **Close**

## Tools and Resources

- **Health Modelling**: [https://learn.microsoft.com/en-gb/azure/well-architected/mission-critical/mission-critical-health-modeling](https://learn.microsoft.com/en-gb/azure/well-architected/mission-critical/mission-critical-health-modeling)
- **Apache JMeter**: [https://jmeter.apache.org/](https://jmeter.apache.org/)
- **Locust**: [https://locust.io/](https://locust.io/)
- **Prometheus**: [https://prometheus.io/](https://prometheus.io/)
- **Grafana**: [https://grafana.com/](https://grafana.com/)
- **Azure Monitor**: [https://azure.microsoft.com/en-us/services/monitor/](https://azure.microsoft.com/en-us/services/monitor/)
- **PagerDuty**: [https://www.pagerduty.com/](https://www.pagerduty.com/)
- **Slack**: [https://slack.com/](https://slack.com/)

## Conclusion

This multi-team event is designed to test the resilience and performance of our application under simulated high-load conditions. By working together and leveraging the strengths within each team, we aim to identify and address potential issues, ensuring a robust and reliable system.

