### Reboot an instance which is created by Auto Scaling Group

Inorder to reboot an instance that is created by an Auto Scaling group (ASG) without creating another instance as a replacement, we can temporarily detach/ standby the instance from the ASG and then perform the reboot. Below showing the procedures for the same.

### 1. Detach and Reboot
### 2. Standby and Reboot

### Detach and reboot

Detaching an EC2 instance from an Auto Scaling group means removing it from the ASG's management and allowing it to operate as a standalone EC2 instance. When an instance is detached from an ASG, it will no longer be automatically scaled or replaced by the ASG.When an instance is detached, it is no longer part of the ASG's scaling activities, such as scaling in or out, health checks, or replacement.

1 ) Open the Amazon EC2 console.
2 ) Navigate to the "Auto Scaling Groups" section.
3) Select the ASG that contains the instance you want to detach.
4) In the "Instances" tab, locate the instance you wish to detach.
5) Select the instance and click on the "Actions" button.
6) Choose the "Detach Instances" option from the drop-down menu.
Please note that while detaching, please uncheck Replace Instance option and please make sure that the minimum group size value must be equal to 0(Zero).

<img width="459" alt="Capture" src="https://github.com/arshadrebin/asg-instances-management/assets/116037443/15331b16-92d1-4d00-b25e-d8763d7f72fb">


After this, we can reboot these insrtance scaling in or out, or replacement.

Activity history is shown as below.

<img width="736" alt="Capture" src="https://github.com/arshadrebin/asg-instances-management/assets/116037443/f2a8a9e5-7e4a-4a15-9158-d7611a71b825">


### Standby and reboot

In AWS Auto Scaling, a standby instance refers to an EC2 instance that is temporarily out of service within an ASG but still part of the Auto Scaling group.Standby instances are useful in scenarios such as performing system maintenance, applying updates, or temporarily reducing capacity while keeping the instance available for future use.
