# continue_test_pipeline_ActiveDeploy
Testing Active Deploy in Delivery Pipeline.

A continue test pipeline automation for pipeline V2 that triggers a given project pipeline having Active Deploy as extensions. It checks the status of the jobs in each pipeline stages and validates if it executed successfully.

Mandatory input parameters:

1. Export 'ibmIdUsername' and 'ibmIdPassword'.

        'ibmIdUsername' is the IBM ID username needed to login onto the system that runs the project pipeline.

        'ibmIdPassword' is the IBM ID password needed to login onto the system that runs the project pipeline.

        Example:
                export ibmIdUsername=<IBM ID psername>
                export ibmIdPassword=<IBM ID password>

2. Set 'Host', 'ProjectName' and 'otcPipelineHost' in the pipeline_test.property file.

        'Host' is the url to Bluemix and is needed for login.

                https://console.ng.bluemix.net

        'ProjectName' is the ID of the Pipeline Project:

              <Pipeline-Project-ID>

        'otcPipelineHost' is the host ot the OTC Pipeline, that hosts the Request Endpoints to retrieve job status infos.

                https://otc-pipeline-server.ng.bluemix.net

        Example for the 'Prod' target:
                [Config]
                Host=https://console.ng.bluemix.net
                ProjectName=<The Pipeline project ID>
                otcPipelineHost=https://otc-pipeline-server.ng.bluemix.net
