# ThermohiGUI – README

## About ThermohiGUI
**ThermohiGUI** is a graphical user interface (GUI) application for calculating activation energy ($E_a$) and exporting the corresponding results (including $E_a$ values and plotting data). Supports MacOS (arm64) and Windows (amd64) and you can download it from any of the following links :):
**site1**: https://drive.google.com/drive/folders/1VGkIb_MzAON_-4iSK3veJabuobJB_w3V?usp=drive_link

**site2**: https://pan.baidu.com/s/15UHJQA5SejSC-qj5V74BTw?pwd=1919

This program implements five widely used non-isothermal kinetic analysis methods: FWO, Starink, KAS, Friedman, and Vyazovkin.
For reliable analysis, at least three heating programs are required.

*While efforts have been made to ensure a robust and user-friendly design (e.g., letter, symbol, zero, and negative number is not allowed in filling heating rate.), users are encouraged to carefully verify the validity and quality of their input data, as these directly affect the reliability of the calculated results.*

ThermohiGUI is designed to lower the barrier for activation energy calculation. Even without programming experience, users can quickly and conveniently obtain $E_a$.

The software is developed by Hikari Quicklime (ORCID: 0000-0002-3318-4921) and is based on the open-source Python package thermohipy (created by Hikari Quicklime, available on PyPI).

I hope this tool can support your research workflow—saving you time for coffee, rest, or more creative work.
### **If you find this program useful, please consider citing our related research publications.🤝**

⸻

### Interface
ThermohiGUI supports multiple languages. Users can select their preferred language within the interface.

**If you would like to suggest improvements or contribute a new language, please contact the author or modify the corresponding JSON file (JSON code could be found at the end).**
![多语言](./pictures/多语言支持.png)

⸻

### Data Export
Analysis results can be exported directly, allowing users to perform further visualization using external tools such as OriginPro or other plotting software.
I plan to add simple drawing functions in the future, as this is also a troublesome repetitive task...if i had more money or time in the future.

**Result interface**
Click on "Export excel file"button, the results will be saved as `xlsx` file and show you the path.
![](./pictures/保存数据.png)
**Fitting results**
![](./pictures/保存数据KAS.png)

**Scatter data for methods except vyazokvin method**
![](./pictures/绘图数据.png)

**Vyazovkin plotting data**
if vyazovkin method is used, the fitting curves are U-shaped:
![vyazovkin.png](./pictures/vyazovkin.png)

⸻

### English-en_US.json

{
    "err_paste_title": "Paste Failed",
    "err_paste_msg": "Only numeric values are allowed.",
    "err_paste": "Paste Failed",
    "add_experiment": "+ Add New Experiment",
    "choose_method": "Method Selection",
    "btn_calc": "Start Calculation",
    "export_xlsx": "Export Excel File (*.xlsx)",
    "close_Return": "Close and Return",
    "type_in_heating_reate": "Enter heating rate (K/min):",
    "type_in_err1": "Input Error",
    "type_in_err1_msg": "Heating rate must be greater than 0. Please re-enter.",
    "warn_repeat": "Duplicate Input",
    "warn_repeat_msg": "Heating rate {path} K/min already exists.\nPlease enter a different value.",
    "type_in_err2": "Input Error",
    "type_in_err2_msg": "Please enter a non-zero numeric value (e.g., 10 or 5.5).",
    "alpha": "Conversion (α)\nSpecified extent of conversion",
    "temp": "Temperature (T)\n(°C)",
    "dadT": "dα/dT\n(Optional if Friedman method is not used)",
    "cal_err": "Calculation Error",
    "cal_err_msg": "Algorithm {path1} failed.\nError: {err_msg}",
    "check_err_1": "⚠ {path} heating programs provided. ICTAC recommends at least 3 programs for kinetic analysis.",
    "check_err_msg1": "❌ In tab {title}, row {row}, column {col_names}: value is 0 (invalid).\n",
    "check_err_msg2": "❌ In tab {title}, row {row}, column {col_names}: invalid character detected.\n",
    "check_err_msg3": "⚠ Tab [{title}] is empty.",
    "check_err_msg4": "⚠ Inconsistent data lengths. Please ensure all data are properly aligned.",
    "export_success": "Export Successful",
    "export_success_msg": "Data saved successfully.\n\nPath:\n{path}\n\nNote: The Excel file includes calculation results and plotting data (data points, slopes, etc.).",
    "err_tips": "Note:",
    "err_tips_msg": "Undefined export method: {methodname}",
    "export_fail": "Export Failed",
    "export_fail_msg": "An error occurred during export:\n{err_msg}",
    "self_test_title": "Data Validation",
    "self_test_pass": "✅ Data validation passed.",
    "self_test_fail": "❌ Data validation failed:",
    "self_test_begin": "All data are valid. Ready to start calculation.",
    "confirm_and_start": "Proceed with Calculation",
    "confirm_and_cancel": "Cancel",
    "confirm_and_modify": "Back to Modify Data",
    "result_title": "Results"
}# thermohiGUI
