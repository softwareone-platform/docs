# Recommendations

The **Recommendations** page is designed to make you aware of the less apparent deficiencies of the infrastructure, like configuration flaws and security risks.&#x20;

## Recommendations interface

In FinOps for Cloud, you can access the **Recommendations** page from the sidebar. On this page, you can review all the recommendations and take action to get the most out of your registered Data Sources.&#x20;

<figure><img src="../../../.gitbook/assets/recommendations.png" alt=""><figcaption></figcaption></figure>

### Data sources <a href="#force-check-and-check-time" id="force-check-and-check-time"></a>

<mark style="color:green;">Displays all data sources in your FinOps for Cloud account. You can select multiple data sources and view all of the recommendations and related metrics for those resources. (New)</mark>

### Summary cards

Use summary cards to view important details, like monthly savings, and last and next check time.&#x20;

* <mark style="color:green;">**Possible monthly savings**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Displays the possible monthly savings that can be achieved if the suggested recommendations were implemented.</mark>
* <mark style="color:green;">**Last check time**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Shows the time when FinOps for Cloud last checked for an update. The system runs a check every 3 hours.</mark>
* <mark style="color:green;">**Next check time**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Indicates when the next recommendation check is due.</mark>&#x20;

<mark style="color:green;">The content of the last summary card varies, depending on the condition. For instance, the card might show any AWS S3 duplicates found during the last check, checks that did not start or finish successfully, and so on. Clicking this specific card opens a summary page, which shows a table containing all checks and the option for you to initiate a new check using</mark> <mark style="color:green;"></mark><mark style="color:green;">**Run check**</mark><mark style="color:green;">.</mark>

### Categories and applicable services <a href="#filtering" id="filtering"></a>

FinOps for Cloud supports different types of recommendations, such as **Savings**, **Security**, **Critical**, and **Non-empty**. By default, the FinOps displays **All** recommendations, but you choose the required category from the **Categories** list.

* <mark style="color:green;">**Savings**</mark> <mark style="color:green;"></mark><mark style="color:green;">-</mark> <mark style="color:green;">These recommendations enable cost savings. For the list of possible recommendations, see</mark> [<mark style="color:green;">Savings Optimization Recommendations</mark>](savings-optimization-recommendations.md)<mark style="color:green;">.</mark>
* <mark style="color:green;">**Security**</mark> <mark style="color:green;"></mark><mark style="color:green;">-</mark> <mark style="color:green;">These recommendations help to improve the security of your data source. For the list of possible recommendations, see</mark> [<mark style="color:green;">Security Recommendations</mark>](security-recommendations.md)<mark style="color:green;">.</mark>
* <mark style="color:red;">**Critical**</mark> <mark style="color:red;"></mark><mark style="color:red;">-</mark>&#x20;
* <mark style="color:red;">**Non-empty**</mark> <mark style="color:red;"></mark><mark style="color:red;">-</mark>&#x20;

&#x20;You can also select an applicable service. <mark style="color:red;">Applicable services represent</mark> &#x20;

### Force check <a href="#force-check-and-check-time" id="force-check-and-check-time"></a>

Currently, the system performs a check every 3 hours and displays the results on the page.

If you have the  Organization Manager role, you can initialize a **Force check** that immediately runs the data sources' evaluation sequence. The option is available in the upper right on the **Recommendations** page. &#x20;

### Recommendations <a href="#color-schema-and-recommendation-cards" id="color-schema-and-recommendation-cards"></a>

Recommendations provide personalized suggestions based on your data, and you can view these recommendations in the form of cards or tables. All recommendations include a description and details related to that recommendation.

To view detailed information about the recommended item, select the card. Pay attention to the color schema of these cards:

* A red outline indicates a critical situation, indicating that you should focus on the card and its information.
* A green outline indicates that there are no recommendations or that potential savings are zero.
* A pale orange outline appears when certain items require attention.

<mark style="color:red;">(To be verified)</mark>

### More options <a href="#settings" id="settings"></a>

The more icon<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAAAXNSR0IArs4c6QAAAw9JREFUeF7tnMuNE0EQhqs6Bx4ZIMGBAOAA0zbIhABEAAJiYREbwUIIrMDugQMEwAEkMuCRwxQarediCTHdas3fZf0+rrq6Zr6va3ddU7YKX1ACCs3O5EIB4ENAARQAJgBOzwqgADABcHpWAAWACYDTswIoAEwAnJ4VQAFgAuD0rAAKABMAp2cFUEAega7rNiKyCSFcM7ObY7Sqfh2G4YeInPd9f563I3a1qwqIMZ6JyKP/IHuTUnqMxTo/uxsBMUabf1siKSUX9+biImOMz0XkZY4AEXmRUjrJjFl8efMC1uv1rWEYPpeQCSHc3m63X0pil4ppXkCM8bWIPCkEcppSeloYu0iYBwEfReROIY1PKaW7hbGLhDUvoOu636p6qYSGmf3p+/5ySexSMc0LiDH+FJErhUB+pZSuFsYuEta8gNVq9d7M7pXQUNUPu93ufknsUjHNC+i67kRVn5UAMbNXfd+P/8I2+/IgYKOq70oImtmD1lsTzQsYwc9sQRw6ctGScCFgL4GtiJJfAzVjZrYkXLQgJi5uKmC64H1r4qGIXDezG+PPVfWbiHwPIbxtvfVweCDdCahZUS3sRQFgCxRAAWAC4PSsAAoAEwCnZwVQAJgAOL27CuBcEPDEzGzKuWjCuWtFcC4Ie/I5F4Tiz7kgFPl9Xs4F4QVwLgjpgHNBSPoXz4M5F4R0wLkgJH0R4VwQXgDngsAOOBeEFjDmZyuiAQucC2pAAueCGpBwTJfg7oHMMcEf74UCwEYpgALABMDpWQEUACYATs8KoIA8ApwLyuNVdTXngqrizNuMzbg8XlVXz2zCHeZ08WG95v8Icy6o6lnO34xzQfnMqkbEGDkXVJVo5macC8oEVns554JqE83cj3NBmcBqL+dcUG2imfuNrQd+X1AmtNrLZ7YgDtO6+KhS82/EJqpsRdQ+1gX7zWxJuGhBTLfvpgKmC+ZcUMHJZci/CbirgGOTSQFgoxRAAWAC4PSsAAoAEwCnZwVQAJgAOD0rgALABMDpWQEUACYATs8KoAAwAXB6VgBYwF/mZEdwBsiwPwAAAABJRU5ErkJggg==" alt="<svg xmlns=&#x22;http://www.w3.org/2000/svg&#x22; height=&#x22;24px&#x22; viewBox=&#x22;0 -960 960 960&#x22; width=&#x22;24px&#x22; fill=&#x22;#434343&#x22;><path d=&#x22;M480-160q-33 0-56.5-23.5T400-240q0-33 23.5-56.5T480-320q33 0 56.5 23.5T560-240q0 33-23.5 56.5T480-160Zm0-240q-33 0-56.5-23.5T400-480q0-33 23.5-56.5T480-560q33 0 56.5 23.5T560-480q0 33-23.5 56.5T480-400Zm0-240q-33 0-56.5-23.5T400-720q0-33 23.5-56.5T480-800q33 0 56.5 23.5T560-720q0 33-23.5 56.5T480-640Z&#x22;/></svg>" data-size="line">contains options that let you configure or update your recommendation settings.

* **Settings** - Adjusting parameters is beneficial because it allows you to fine-tune and optimize results to better meet specific goals or conditions. The set of parameters varies depending on the card, so set the values according to your needs. New settings are applied during the next recommendations check.
* <mark style="color:green;">**Exclude pools**</mark> <mark style="color:green;"></mark><mark style="color:green;">- Allows you to choose all the pools you want to exclude from the specific recommendation. When excluded, you'll see the list of excluded objects in the</mark> <mark style="color:green;"></mark><mark style="color:green;">**Excluded**</mark> <mark style="color:green;"></mark><mark style="color:green;">tab on the</mark> <mark style="color:green;"></mark><mark style="color:green;">**Recommendations**</mark> <mark style="color:green;"></mark><mark style="color:green;">page.</mark>
* <mark style="color:green;">**Pin or unpin a recommendation**</mark> <mark style="color:green;"></mark><mark style="color:green;">- You can pin a recommendation by selecting</mark> <mark style="color:green;"></mark><mark style="color:green;">**Pin**</mark><mark style="color:green;">. Once pinned, the recommendation will always appear as the first one in your list of recommendations until you</mark> <mark style="color:green;"></mark><mark style="color:green;">**Unpin**</mark> <mark style="color:green;"></mark><mark style="color:green;">it. The option to pin a recommendation is only available in the card view.</mark>&#x20;
