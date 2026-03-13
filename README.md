# acit4640-lab10

## Team

- Angad Bains
- Misha Makaroff

## create new keys

```bash
ssh-keygen -t ed25519 -f ~/.ssh/aws
```

This command will create the ssh key in the .ssh directory of the user. It will create a `aws` private key and a `aws.pub` public key.

## run included scripts to import and delete keys

```bash
./scripts/import_lab_key /home/anges/.ssh/aws.pub
```

This will add the newly created key to our logged in aws account.

```bash
./scripts/delete_lab_key
```

This removes the key from our aws account, as it is no longer needed.

## terraform commands

```bash
cd terraform/
terraform init
terraform apply
```

Using these commands we initialize terraform at the location where our terraform configuration (main.tf) is present. `Apply` allows us to create the ec2 instances as configured in our terraform file.

## Creating Roles

```bash
ansible-galaxy role init rocky
```

```bash
ansible-galaxy role init debian
```