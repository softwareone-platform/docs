# Clean-up Scripts Based on Recommendations

{% hint style="danger" %}
The script deletes all recommended resources (based on the downloadable JSON file) and ignores errors. After completion, a summary lists deleted resources, non-existing or already deleted resources, and resources that couldn't be deleted due to other reasons.
{% endhint %}

## Amazon Web Services (AWS) <a href="#aws-source" id="aws-source"></a>

{% tabs %}
{% tab title="Prerequisites" %}
* [AWS Command Line Interface (AWS CLI)](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
* jq - The package allows executing JSON scripts with bash. See [Download jq](https://stedolan.github.io/jq/download/).
{% endtab %}

{% tab title="Implementation" %}
1. Install the requirements on a machine running Linux OS.
2. Configure the AWS Command Line Interface. (Run the **aws configure** command. For information, see the [AWS User Guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html)).
3. Download the script from the corresponding subsection on the **Recommendations** page.
4. From the same page, download the JSON file containing a list of all resources recommended for deletion.
5. Run the script as follows: `bash <script_name> <path to json file>.`
{% endtab %}
{% endtabs %}

## Microsoft Azure <a href="#azure-source" id="azure-source"></a>

{% tabs %}
{% tab title="Prerequisites" %}
* [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=apt)
* jq - The package allows executing JSON scripts with bash. See [Download jq](https://stedolan.github.io/jq/download/).
{% endtab %}

{% tab title="Implementation" %}
### Azure Azure CLI

1. Install the requirements on a machine running Linux OS.
2. Sign in with the Azure CLI.
3. Download the script from the corresponding subsection of the Recommendations page.
4. From the same page, download the JSON file containing a list of all resources that are recommended for deletion.
5. Run the script as follows: `bash <script_name> <path to json file>`.

### Azure Shell

1. Open [Azure Cloud Shell](https://portal.azure.com/#cloudshell/).
2. Download the script and the JSON file from the corresponding subsection of the Recommendations page.
3. Copy these files using the **Upload/Download files** button. The files will be placed in `/usr/csuser/clouddrive`.
4. Run the script as follows: `bash <script_name> <path to json file>` using absolute paths or navigate to the necessary folder before executing.
{% endtab %}
{% endtabs %}

## Google Cloud Platform (GCP)

{% tabs %}
{% tab title="Prerequisites" %}
[Google Cloud CLI](https://cloud.google.com/sdk/gcloud)

jq - The package allows executing JSON scripts with bash. See [Download jq](https://stedolan.github.io/jq/download/).
{% endtab %}

{% tab title="Implementation" %}
1. Install requirements on a machine running Linux OS.
2. Configure gcloud: run gcloud init. See [Initializing the gcloud CLI](https://cloud.google.com/sdk/docs/initializing) for more information.
3. Run script bash `<script_name> <path to recommendation json file>`.
{% endtab %}
{% endtabs %}
