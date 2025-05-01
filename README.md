In this project, I have built a **CoWIN Dashboard App** by applying the concepts I have learned till now.

### Refer to the images below for Output:

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-output.gif" alt="cowin-dashboard-output" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

**Failure View**

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-failure-view-output.gif" alt="cowin-dashboard-failure-view-output" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

### Design Files

<details>
<summary>Click to view</summary>

- [Extra Large Devices (Size >= 1200px) - Success View](https://assets.ccbp.in/frontend/content/react-js/cowin-dashboard-xl-output.png)
- [Extra Large Devices (Size >= 1200px) - Failure View](https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-xl-failure-view-output.png)

</details>

### Set Up Instructions

<details>
<summary>Click to view</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`

</details>

### Completed Following Instructions

<details>
<summary>Functionality added</summary>
<br/>

The app has the following functionalities:

- When the page loads, an HTTP GET request is made to `https://apis.ccbp.in/covid-vaccination-data`
- A loader is displayed while the request is in progress
- Upon successful data retrieval:
  - A **Bar Chart** is used to show vaccination coverage over the last 7 days
  - Two **Pie Charts** are used to display:
    - Vaccination by gender
    - Vaccination by age
- If the request fails, a **Failure View** image is shown

</details>

<details>
<summary>API Requests & Responses</summary>
<br/>

**covidVaccinationDataApiUrl**

#### API: `https://apis.ccbp.in/covid-vaccination-data`

#### Method: `GET`

#### Description:

Returns a response with vaccination statistics

#### Success Response:

```json
{
  "last_7_days_vaccination": [
    {
      "vaccine_date": "30th Jul",
      "dose_1": 3757930,
      "dose_2": 1817805
    },
    ...
  ],
  "vaccination_by_age": [
    {
      "age": "18-44",
      "count": 482792375
    },
    ...
  ],
  "vaccination_by_gender": [
    {
      "count": 4809680,
      "gender": "Male"
    },
    ...
  ]
}
```

</details>

<details>
<summary>Components Structure</summary>

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/cowin-dashbaord-component-structure-breakdown.png" alt="component-breakdown-structure" style="max-width:100%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

</details>

<details>
<summary>Implementation Files</summary>
<br/>

Used these files to complete the implementation:

- `src/components/CowinDashboard/index.js`
- `src/components/CowinDashboard/index.css`
- `src/components/VaccinationCoverage/index.js`
- `src/components/VaccinationCoverage/index.css`
- `src/components/VaccinationByGender/index.js`
- `src/components/VaccinationByGender/index.css`
- `src/components/VaccinationByAge/index.js`
- `src/components/VaccinationByAge/index.css`

</details>

### Important Note

<details>
<summary>Click to view</summary>

<br/>

- Loader is wrapped with a container and has `data-testid="loader"`:

  ```jsx
  <div data-testid="loader">
    <Loader type="ThreeDots" color="#ffffff" height={80} width={80} />
  </div>
  ```

- Charts are provided with `width` and `height` as **numbers**:

  ```jsx
  <BarChart width={1000} height={300} />
  ```

- Achieved this layout for desktop devices using the `recharts` library with customized props

</details>

### Resources Used

<details>
<summary>Image URLs</summary>

- [https://assets.ccbp.in/frontend/react-js/api-failure-view.png](https://assets.ccbp.in/frontend/react-js/api-failure-view.png) – alt: **failure view**
- [https://assets.ccbp.in/frontend/react-js/cowin-logo.png](https://assets.ccbp.in/frontend/react-js/cowin-logo.png) – alt: **website logo**

</details>

<details>
<summary>Colors</summary>

<br/>

<div style="background-color: #161625; width: 150px; padding: 10px; color: white">Hex: #161625</div>
<div style="background-color: #2cc6c6; width: 150px; padding: 10px; color: black">Hex: #2cc6c6</div>
<div style="background-color: #cbd5e1; width: 150px; padding: 10px; color: black">Hex: #cbd5e1</div>
<div style="background-color: #ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
<div style="background-color: #1c1c2b; width: 150px; padding: 10px; color: white">Hex: #1c1c2b</div>
<div style="background-color: #2d87bb; width: 150px; padding: 10px; color: black">Hex: #2d87bb</div>
<div style="background-color: #a3df9f; width: 150px; padding: 10px; color: black">Hex: #a3df9f</div>
<div style="background-color: #64c2a6; width: 150px; padding: 10px; color: black">Hex: #64c2a6</div>
<div style="background-color: #94a3b8; width: 150px; padding: 10px; color: black">Hex: #94a3b8</div>
<div style="background-color: #f54394; width: 150px; padding: 10px; color: black">Hex: #f54394</div>
<div style="background-color: #5a8dee; width: 150px; padding: 10px; color: black">Hex: #5a8dee</div>
<div style="background-color: #2cc6c6; width: 150px; padding: 10px; color: black">Hex: #2cc6c6</div>
<div style="background-color: #6c757d; width: 150px; padding: 10px; color: black">Hex: #6c757d</div>

</details>

<details>
<summary>Font-families</summary>

- Roboto

</details>

### Conclusion

- 💉 This project demonstrates the use of `recharts`, API data handling, and conditional rendering to build a responsive and data-driven CoWIN Dashboard.
- Thanks for checking out my CoWIN Dashboard App! It showcases my skills in API integration, chart rendering, and responsive layout with React.

- 🔗 Check it out here: [https://cowindashboard.ccbp.tech]

Happy coding! 🚀
