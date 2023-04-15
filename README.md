This template creates a security group and optionally grants it access to make https calls to another sg.

If you create a second stack from this template and give the name of the 1st stack,
the 2nd stack adds a rule into the sg of the 1st stack granting access for resources
which may use second sg to make https calls to resources using the 1st sg.

The learning goal of this stack is to facilitate learning about via experimentation re:
stack updates, rollback, and template linking, to name a few ways it could be used.

Here are some ideas:
1. Deploy an initial stack that only has a vpc id
2. Explore the Resources and Outputs tabs of that stack
3. View the security group in the EC2 or VPC console UI
4. Deploy a second stack and give the name of the first stack
5. Explore the Resources tab of the second stack and the ingress rules of the two security groups
6. Delete the 1st stack. (Hint: This should fail because the stack's Output is referenced)
7. Explore the Exports section of the CloudFormation console
8. Click on the exports and see how they differ (one is imported, one is not)
9. Do a stack update on the second stack and blank out the StackName parameter (this shows you can change the stack links and delete the conditional resource without deleting the entire stack)

The above steps are an idea - there are plenty of other ways you can explore various aspects of CloudFormation.
For example, add a tag onto one of the stacks and observe how it updates its resources. How is this similar to and different from the Tags property declared in the template itself?
And another example, create a change set on an already-created stack - this simple template can be a vehicle for learning about how change sets work.

Finally, have fun!

By: J Frear on 2023-04-14
