# mytest
robotframework 测试用例集
测试用例1:百度搜索
*** Settings ***
Library           Selenium2Library

*** Test Cases ***
Login
    [Documentation]    This is testing for Selenium2Library webdrvier
    Open Browser    http://www.baidu.com    chrome
    Input Text    id=kw   简书 robotframework
    Click button    id = su
    sleep    2
    ${title}    Get Title
    should contain    ${title}    robotframework
    close Browser

