# Deploy CP4BA 

1) Download and extract the attached zip file
2) cd to terraform-ibm-cloud-pak/modules
3) update the parameter values in  terraform.tfvars file from cp4ba/test/stages. Make sure to provide all the details and stroage classes. 
4) Execute automation script either using docker or from your local machine. 

Using the following docker image to execute the automation is  easiest way because all the required runtimes (like terraform, oc, ibmcloud cli, etc ) are already installed within the image.

    a) bring the docker container

    docker run -it \
    -v ${PWD}:/terraform \
    -w /terraform \
    quay.io/cloudnativetoolkit/cli-tools

    b) with in container, 
    cd cb4ba/test/stages

    c) execute the below
    terraform init
    terraform apply
    when prompted, provide Yes to proceed
