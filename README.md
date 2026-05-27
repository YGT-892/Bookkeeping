# 本地记账功能说明 / Local Bookkeeping Guide

## 简介 / Overview

本地记账是一个本地优先的个人账本。它围绕账户余额、日常流水、事件摊销、资产变化和分类管理工作。数据保存在本机浏览器或桌面应用的本地数据库中；当前版本支持手动记账、编辑、导出和清除数据，不支持导入数据。

Local Bookkeeping is a local-first personal ledger. It is built around account balances, daily transactions, event amortization, asset history, and category management. Data is stored in the local database of the browser or desktop app. The current version supports manual entry,本地记账功能说明 / Local Bookkeeping Guide

简介 / Overview

本地记账是一个本地优先的个人账本。它围绕账户余额、日常流水、事件摊销、资产变化和分类管理工作。数据保存在本机浏览器或桌面应用的本地数据库中；当前版本支持手动记账、编辑、导出和清除数据，不支持导入数据。

Local Bookkeeping is a local-first personal ledger. It is built around account balances, daily transactions, event amortization, asset history, and category management. Data is stored in the local database of the browser or desktop app. The current version supports manual entry, editing, export, and clearing data; it does not support data import.

核心原则：

Core principles:





账户余额是资产统计的基础。 / Account balances are the basis of asset statistics.



普通流水会影响账户余额。 / Regular transactions affect account balances.



平账记录是某一天结束时的余额锚点。 / A reconcile record is a balance anchor at the end of a specific day.



建账记录是新建账户时自动产生的初始平账。 / An account-opening record is the initial reconcile record automatically created with a new account.



资产历史可以基于未来或过去的平账锚点反推。 / Asset history can be inferred forward or backward from past or future reconcile anchors.



事件和摊销只影响统计口径，不改变原始流水金额。 / Events and amortization affect reporting only; they do not change the original transaction amount.

顶部导航 / Top Navigation

顶部标题显示应用名称。本地网页版本和桌面版使用同一套页面。

The top title shows the app name. The local web version and the desktop version use the same pages.

导航按钮包括：

Navigation buttons include:





总览：查看资产、现金流、资产变化和快速记账。 / Overview: view assets, cash flow, asset changes, and quick entry.



账户：创建、编辑和删除账户。 / Accounts: create, edit, and delete accounts.



流水：查看、过滤、编辑和删除交易流水，也可以查看事件流水。 / Transactions: view, filter, edit, and delete transaction records, and view event records.



设置：管理汇率、语言、分类、账户类型、商户、导出和清除数据。 / Settings: manage FX rates, language, categories, account types, vendors, export, and clearing data.

非设置页右上角显示中文/英文切换。设置页同一位置显示“查看升级”，用于未来桌面版自动升级；网页版本不会执行升级。

On non-settings pages, the top-right control switches between Chinese and English. On the settings page, the same position shows "Check updates" for future desktop auto-updates; the web version does not perform updates.

总览页面 / Overview Page

总览页由三列组成：资产概览、资产与支出图表、快速记账。

The overview page has three columns: asset overview, asset and expense charts, and quick entry.

资产概览卡片 / Asset Overview Card

资产概览展示当前账本的核心资产指标。

The asset overview shows the main asset metrics of the current ledger.

内容包括：

Contents include:





净资产：资产合计减去负债合计，以 USD 显示，并显示 CNY 折算值。 / Net worth: total assets minus total liabilities, shown in USD with a CNY equivalent.



资产合计：所有实体资产和虚拟资产的合计价值。 / Total assets: the total value of all fiat and virtual assets.



负债合计：所有负债账户的合计债务。 / Total liabilities: the total debt across all liability accounts.



法币资产：实体资产账户折算后的总额。 / Fiat assets: the converted total of fiat asset accounts.



虚拟资产：积分、里程、代币等虚拟资产按单价折算后的总额。 / Virtual assets: the converted value of points, miles, tokens, and other virtual assets based on unit price.

下方资产条形图展示负债、法币资产和虚拟资产在同一坐标轴上的位置。负债在零点左侧，资产在零点右侧。条图上方有一条与条形同一 X 比例的大类色带（负债 / 法币 / 虚拟），与下方堆叠条对齐。

The asset bar chart places liabilities, fiat assets, and virtual assets on one axis. Liabilities sit left of zero and assets to the right. A macro ribbon above the bar uses the same horizontal scale as the stacked segments.

横轴刻度线与金额标签共用同一套选点规则：始终显示左右端点；在间距允许时显示法币与虚拟资产分界及零点（零点优先级最低，避免与分界标签重叠）。

Tick lines and amount labels share one picker: endpoints are always shown; the fiat/virtual boundary and zero are labeled when space allows (zero is lowest priority).

坐标轴数值固定保留两位小数。标题旁「隐藏金额」会同时隐藏 KPI、条图刻度与数字；悬停条图仍可按分类查看结构，金额在隐藏模式下为占位符。

Axis values use two decimal places. Hide amounts masks KPIs and bar tick labels; hovering still shows segment structure with masked amounts.

图例分两层：

The legend has two levels:





上层大类图例：负债、法币资产、虚拟资产。 / Top-level legend: liabilities, fiat assets, and virtual assets.



下层细分图例：按账户类型或自定义账户类型显示。 / Detail legend: displayed by account type or custom account type.

悬停条图时，悬浮窗以大类为一级标题、各账户子类型为二级行显示金额。

The bar tooltip lists each macro group as a heading and account subtypes as indented lines.

底部说明文字提示总览使用设置中的有效 USD/CNY 汇率。

The note at the bottom indicates that the overview uses the effective USD/CNY rate from settings.

资产变化卡片 / Asset Change Card

资产变化展示一段时间内的资产结构趋势。

Asset change shows the trend of asset structure over a selected period.

图表内容：

Chart contents:





负债：以负方向显示。 / Liabilities: shown in the negative direction.



法币资产：以柱状堆叠显示。 / Fiat assets: shown as stacked bars.



虚拟资产：以柱状堆叠显示。 / Virtual assets: shown as stacked bars.



净资产：以折线显示。 / Net worth: shown as a line.

时间范围按钮包括：

Time range buttons include:





4月 / 4 months



8月 / 8 months



1年 / 1 year



3年 / 3 years



YTD / YTD



自选 / Custom

自选范围会显示开始和结束日期选择框（自定义日历，宽度较宽裕以免日期错行）。图表按半月采样，适合观察长期变化。

The custom range shows start and end date pickers (custom calendar, wider fields to avoid wrapped dates). The chart samples roughly every half month, making it suitable for long-term trends.

资产历史的计算逻辑：

Asset history calculation logic:





如果某日之前有平账锚点，从该锚点向后累加流水。 / If there is a reconcile anchor before a day, the system starts from that anchor and adds later transactions.



如果某日之后有平账锚点，从未来锚点向前反推余额。 / If there is a reconcile anchor after a day, the system starts from the future anchor and infers the earlier balance backward.



新建账户自动有“建账”锚点，因此建账前的流水可以反推出更早余额。 / A new account automatically has an account-opening anchor, so transactions before account opening can infer earlier balances.

悬停资产变化图时，悬浮窗同样采用大类一级、子类二级结构（负债 / 法币 / 虚拟及其账户子类型）。

The asset-trend tooltip uses the same macro heading + subtype lines layout.

本周支出卡片 / This Week Expense Card

本周支出卡片展示本周现金流摘要和支出分类饼图。

The this-week expense card shows this week's cash flow summary and expense category pie chart.

内容包括：

Contents include:





收入 / Income



支出 / Expenses



净流入/净支出 / Net inflow or net outflow



本周支出饼图 / This-week expense pie chart



共享分类图例 / Shared category legend



「隐藏金额」按钮（与饼图、图例悬浮窗联动）/ Hide amounts toggle (linked to pie and legend tooltips)

转账和平账不会计入现金流。普通收入和支出会计入。启用每日摊销的流水会按设置的日期区间分摊到每一天，用于本周、本月、本年统计。

Transfers and reconcile records are not counted as cash flow. Regular income and expenses are counted. Transactions with daily amortization enabled are spread across the configured date range and used in weekly, monthly, and yearly statistics.

本月支出卡片 / This Month Expense Card

本月支出卡片展示本月支出分类饼图和本月现金流摘要。

The this-month expense card shows this month's expense category pie chart and cash flow summary.

内容包括：

Contents include:





本月收入 / This-month income



本月支出 / This-month expenses



本月净额 / This-month net amount



本月支出分类饼图 / This-month expense category pie chart

本周（及同布局的支出卡）在无支出数据时，右侧会显示垂直居中的空状态提示。

When there is no expense data, an empty-state message appears vertically centered in the chart area.

本年支出卡片 / This Year Expense Card

本年支出卡片展示本年支出分类饼图和本年现金流摘要。

The this-year expense card shows this year's expense category pie chart and cash flow summary.

内容包括：

Contents include:





本年收入 / This-year income



本年支出 / This-year expenses



本年净额 / This-year net amount



本年支出分类饼图 / This-year expense category pie chart

本年统计同样遵守事件摊销逻辑。

Yearly statistics also follow the event amortization logic.

支出饼图悬浮窗： 悬停本周 / 本月 / 本年任意扇区时，列出该周期全部分类（金额在上、占比在下，按金额从高到低）。超过 5 个分类时向右增加列，列间有竖线分隔，不使用滚动条。开启「隐藏金额」时，金额与占比均显示为 •••。

Expense pie tooltips: Hovering any slice on the week/month/year pies lists all categories for that period (amount above, percent below, sorted by amount). More than five categories add columns to the right with vertical dividers—no scrollbar. With hide amounts on, values show as •••.

本周图例悬停： 鼠标悬停某一分类图例时，显示该分类的本周 / 本月 / 本年金额（同样受「隐藏金额」控制）。图例文字为默认箭头光标。

Weekly legend hover: Hovering a legend item shows that category’s week / month / year amounts (respects hide amounts). The legend uses the default arrow cursor.

快速记账卡片 / Quick Entry Card

快速记账用于快速新增支出、收入或转账。

Quick entry is used to quickly add expenses, income, or transfers.

支出字段包括：

Expense fields include:





类型 / Type



账户 / Account



日期 / Date



大类 / Main category



明细 / Detail category



商户 / Vendor



金额 / Amount



每日摊销 / Daily amortization



特定事件 / Specific event



备注 / Notes

收入字段包括：

Income fields include:





类型 / Type



账户 / Account



日期 / Date



大类 / Main category



明细 / Detail category



商户 / Vendor



金额 / Amount



每日摊销 / Daily amortization



特定事件 / Specific event



备注 / Notes

转账字段包括：

Transfer fields include:





类型 / Type



转出账户 / Source account



转入账户 / Target account



日期 / Date



金额 / Amount



备注 / Notes

账户下拉列表展开时按资产大类和账户类型分组。选中后只显示账户名称。转账支持：

When the account dropdown is expanded, accounts are grouped by asset group and account type. After selection, only the account name is shown. Supported transfers include:





实体资产到实体资产。 / Fiat asset to fiat asset.



实体资产到负债，用于信用卡还款。 / Fiat asset to liability, used for credit card repayment.



负债到实体资产，用于取现或借款入账。 / Liability to fiat asset, used for cash advance or loan proceeds.



实体资产或负债到虚拟资产，用于购买积分、礼品卡、里程等。 / Fiat asset or liability to virtual asset, used to buy points, gift cards, miles, and similar assets.



虚拟资产到虚拟资产，用于积分或里程转换。 / Virtual asset to virtual asset, used for points or miles conversion.

保存时若金额无效、超过额度或余额不足、未选日期、摊销日期缺失、部分必填项未填等，会以与「清除全部数据」相同的确认弹窗提示（多条校验可合并为一段多行文案，非表单下方红字）；文案随当前界面语言显示。

Blocking errors (invalid amount, credit limit, insufficient balance, missing date, missing amortization dates, required fields, and similar) use the same confirm modal as clear-all; multiple issues may appear in one multi-line message. Messages follow the UI language.

事件名： 与已有事件名称相同（不区分大小写）时，流水会归入该事件，事件流水中的笔数与摊销统计随之更新。

Event names: Matching an existing event name (case-insensitive) links the transaction to that event and updates counts and amortized totals.

流水页面 / Transactions Page

流水页分为交易流水和事件流水两个视图。

The transactions page has two views: transaction records and event records.

交易流水视图 / Transaction Records View

交易流水列表展示每一笔原始交易。

The transaction list shows each original transaction.

表格列包括：

Table columns include:





日期 / Date



账户 / Account



类型 / Type



分类 / Category



事件 / Event



商户 / Vendor



金额 / Amount



操作 / Actions

账户列会显示资产大类，例如“实体资产 · Chase”。转账会显示转出与转入两侧，例如“实体资产 · Chase → 负债 · CFU”。

The account column shows the asset group, for example "Fiat assets · Chase". Transfers show both source and target sides, for example "Fiat assets · Chase → Liability · CFU".

类型包括：

Types include:





支出 / Expense



收入 / Income



转账 / Transfer



平账 / Reconcile

平账不能在流水编辑弹窗中改为普通交易。建账记录属于平账的一种，分类显示为“建账”。

A reconcile record cannot be changed into a regular transaction in the transaction edit dialog. An account-opening record is a type of reconcile record, and its category is shown as "Account opening".

筛选器包括：

Filters include:





类型 / Type



商户关键词 / Vendor keyword



分类大类 / Main category



分类明细 / Detail category



账户大类 / Account group



账户 / Account



开始日期 / Start date



结束日期 / End date

当上级筛选条件变化时，相关下级筛选会自动清空，避免选择不存在的组合。

When a parent filter changes, related child filters are cleared automatically to avoid invalid combinations.

编辑流水 / Editing Transactions

支出和收入流水可以编辑：

Expense and income transactions can edit:





账户 / Account



日期 / Date



分类 / Category



商户 / Vendor



金额 / Amount



摊销 / Amortization



事件 / Event



备注 / Notes

转账流水可以编辑：

Transfer transactions can edit:





转出账户 / Source account



转入账户 / Target account



日期 / Date



金额 / Amount



备注 / Notes

编辑会撤销旧流水对余额的影响，再应用新流水，并重新根据平账锚点计算受影响账户余额。

Editing first reverses the old transaction's balance effect, then applies the new transaction, and finally recomputes affected account balances based on reconcile anchors.

删除普通流水会移除该流水并重算账户余额。若该流水是某事件下最后一笔关联的支出/收入，事件记录会自动删除（事件流水笔数归零）。删除建账流水会触发二次确认；确认后会删除对应账户及相关流水。

Deleting a regular transaction removes the row and recomputes balances. If it was the last expense/income row linked to an event, the event record is removed automatically. Deleting an account-opening row uses a second confirmation and deletes the account and related rows.

事件流水视图 / Event Records View

事件流水把被标记为同一事件的交易汇总展示。事件名称相同（不区分大小写）的流水会归入同一事件；在流水编辑里把事件名改成与另一条事件相同，也会合并。

Event records group transactions under one event. The same event name (case-insensitive) links rows together; editing a transaction’s event name to match another event merges them.

每个事件会显示：

Each event shows:





事件名称 / Event name



事件日期范围 / Event date range（随关联流水与摊销区间自动汇总） / (spans all linked rows and amortization ranges)



关联交易数量 / Number of linked transactions



原始总额 / Original total



本周摊销额 / This-week amortized amount



本月摊销额 / This-month amortized amount



本年摊销额 / This-year amortized amount

界面不再显示事件类型、周期列；编辑事件时也不可修改类型/周期（后台仅保留默认字段以兼容旧数据）。

The UI no longer shows event type or cadence columns; the event editor does not expose them (defaults are kept for compatibility).

点击「编辑」可修改名称、日期范围与备注，或删除事件（两步确认）。删除事件不会删除流水，只会解除关联与摊销，流水变为普通一次性记录。

Edit opens name, date range, and notes, or delete event (two-step confirm). Deleting an event does not delete transactions; it clears event links and amortization flags only.

「查看明细」可跳到交易流水并筛选该事件。事件用于统计归集，不直接改变账户余额。

View details filters transaction records by that event. Events affect reporting only, not ledger balances.

账户页面 / Accounts Page

账户页面按资产大类分三列：

The accounts page is divided into three columns by asset group:





实体资产 / Fiat assets



虚拟资产 / Virtual assets



负债 / Liabilities

每列显示该类账户列表和合计金额。账户卡片显示：

Each column shows accounts in that group and the group total. An account card shows:





账户名称 / Account name



账户类型 / Account type



币种 / Currency



余额或数量 / Balance or quantity



折算值 / Converted value



编辑按钮 / Edit button

新建账户逻辑 / New Account Logic

新建账户时需要填写：

When creating an account, fill in:





账户名称 / Account name



账户大类与账户类型 / Account group and account type



币种 / Currency



初始余额 / Opening balance



虚拟资产单价 / Virtual asset unit price



负债额度 / Liability credit line



备注 / Notes

新建账户本身会自动生成一条“建账”平账记录。建账日期戳记为创建当日的明天。这样当你在建账日期之前补录交易时，系统可以从建账余额向前反推历史余额。

Creating an account automatically creates an "account opening" reconcile record. The account-opening date stamp is tomorrow relative to the creation date. This lets the system infer earlier balances backward from the opening balance when you add transactions before the opening date.

编辑账户逻辑 / Account Editing Logic

未勾选“记录为平账”时，编辑账户只修改账户资料，例如：

When "Record as reconcile" is not checked, editing an account only changes account details, such as:





名称 / Name



类型 / Type



币种 / Currency



虚拟资产单价 / Virtual asset unit price



信用额度 / Credit line



备注 / Notes

勾选“记录为平账”时，当前填写的余额会作为所选日期结束时的余额锚点。系统会创建一条平账流水，并根据该锚点重算账户余额。

When "Record as reconcile" is checked, the entered balance becomes the balance anchor at the end of the selected date. The system creates a reconcile transaction and recomputes the account balance from that anchor.

平账的作用：

The purpose of reconcile records:





固定某一天结束时的真实余额。 / Fix the real balance at the end of a specific day.



让之后的流水向后推算余额。 / Let later transactions calculate balances forward.



让之前的流水向前反推余额。 / Let earlier transactions infer balances backward.

删除账户 / Deleting Accounts

若账户仅有建账流水（无其它支出、收入、转账等），可在编辑账户时点「删除」；删除后底部出现 10 秒撤销 提示，与设置页删除分类/商户一致。

If an account has only the opening reconcile row, you can delete it from the account editor; a 10-second undo toast appears afterward, same as settings deletions.

若仍有其它流水，需先在流水页删除或改账后再删账户。在流水页删除建账记录时，会二次确认并删除该账户及其相关流水。

If other transactions exist, remove or reassign them first. Deleting an opening reconcile row from the transactions page still uses a second confirmation and deletes the account and related rows.

新建信用卡账户须填写信用卡额度；期初欠款不能超过额度。

New credit card accounts require a credit line; opening debt cannot exceed it.

设置页面 / Settings Page

设置页包含左侧基础设置、中间分类管理、右侧账户类型和商户管理。

The settings page contains basic settings on the left, category management in the middle, and account type plus vendor management on the right.

汇率卡片 / FX Rate Card

汇率卡片控制 USD/CNY 折算。

The FX rate card controls USD/CNY conversion.

内容包括：

Contents include:





当前有效汇率 / Current effective rate



最近 API 汇率 / Latest API rate



上次刷新时间 / Last refresh time



手动汇率输入框 / Manual rate input



保存覆盖 / Save override



从 Frankfurter 刷新 / Refresh from Frankfurter

如果设置了手动汇率，总览和账户折算会优先使用手动汇率。留空则使用最近 API 汇率或默认值。

If a manual rate is set, overview and account conversions use the manual rate first. If left blank, the app uses the latest API rate or the default value.

数据导出和清除卡片 / Data Export and Clear Card

当前版本支持：

The current version supports:





导出 Excel / Export Excel



清除全部数据 / Clear all data

导出 Excel 用于备份当前账本。清除全部数据会二次确认，并清空账户、流水、事件、商户和汇率数据。

Export Excel is used to back up the current ledger. Clear all data asks for confirmation twice and clears accounts, transactions, events, vendors, and FX data.

当前版本不支持导入数据。

The current version does not support data import.

地址、时区与语言卡片 / Region, Timezone, and Language Card

该卡片显示当前浏览器检测到的时区（中文界面为友好名称 + UTC±N 偏移，英文界面为英文名称 + 偏移），并提供中文和英文界面切换。

This card shows the detected timezone (friendly name + UTC±N offset in Chinese; English name + offset in English) and provides Chinese and English switching.

日期字段使用应用内 YYYY-MM-DD 日历选择器：点击打开日视图；点标题栏可下钻到月选择，再点年份进入年选择（每页 12 个年份，左右箭头切换年份段）；底部支持清除与「今天」。中文界面为 YYYY/MM/DD 显示、周一起始，英文为 MM/DD/YYYY、周日起始。日期输入与存储按本机时区的日历日处理。

Date fields use an in-app YYYY-MM-DD picker. Open the day grid; click the caption for month selection, then the year for a year grid (12 years per page, prev/next arrows for other ranges). Footer actions: Clear and Today. Chinese UI shows YYYY/MM/DD with Monday first; English shows MM/DD/YYYY with Sunday first. Values use local calendar dates.

分类管理卡片 / Category Management Card

分类管理用于管理支出和收入分类。

Category management is used to manage expense and income categories.

功能包括：

Features include:





支出/收入切换 / Expense and income toggle



搜索分类 / Search categories



编辑模式 / Edit mode



新增自定义大类 / Add custom main category



新增自定义明细 / Add custom detail category



隐藏默认大类或默认明细 / Hide built-in main or detail categories



删除自定义大类或明细 / Delete custom main or detail categories



拖拽调整顺序 / Drag to reorder



撤销删除 / Undo deletion

默认支出分类采用当前标准分类，不支持导入旧分类。

The default expense categories use the current standard taxonomy. Old imported categories are not supported.

账户类型管理卡片 / Account Type Management Card

账户类型管理用于维护账户的子类型。

Account type management is used to maintain account subtypes.

功能包括：

Features include:





实体资产、虚拟资产、负债三类切换 / Toggle between fiat assets, virtual assets, and liabilities



搜索账户类型 / Search account types



编辑模式 / Edit mode



新增自定义账户类型 / Add custom account type



隐藏默认账户类型 / Hide built-in account type



删除未被账户使用的自定义账户类型 / Delete custom account types that are not used by any account



拖拽调整顺序 / Drag to reorder

非编辑模式：类型名称与「内置/自定义 · 使用数」同一行。点击「编辑」后，名称与说明分两行显示，并出现删除按钮。

In normal mode, the type name and “built-in/custom · count” stay on one line. In edit mode, they stack on two lines with a delete button.

账户列表、账户编辑、快速记账下拉和总览图例都会使用这里的账户类型名称。

The account list, account editing, quick-entry dropdown, and overview legend all use account type names from this card.

商户管理卡片 / Vendor Management Card

商户管理展示系统记录过的商户名称。

Vendor management shows vendor names recorded by the system.

功能包括：

Features include:





搜索商户 / Search vendors



编辑模式 / Edit mode



删除商户 / Delete vendors



撤销删除 / Undo deletion

非编辑模式：商户名称与「大类 › 子类」同一行。编辑模式下名称与分类分两行，右侧为删除按钮。

In normal mode, vendor name and category stay on one line. In edit mode, they stack on two lines with delete on the right.

商户用于快速记账自动补全，也用于按商户筛选流水。

Vendors are used for quick-entry autocomplete and for filtering transactions by vendor.

记账和余额计算逻辑 / Transaction and Balance Logic

支出 / Expense

支出会减少实体资产或虚拟资产余额。对于负债账户，支出会增加负债余额。

An expense reduces a fiat asset or virtual asset balance. For a liability account, an expense increases the liability balance.

收入 / Income

收入会增加实体资产或虚拟资产余额。对于负债账户，收入可作为还款，会减少负债余额。

Income increases a fiat asset or virtual asset balance. For a liability account, income can act as repayment and reduce the liability balance.

转账 / Transfer

转账不计入支出或收入统计。它只在账户之间移动余额。

Transfers are not counted as income or expenses. They only move balances between accounts.

常见转账：

Common transfers:





实体资产到实体资产：例如银行账户之间转钱。 / Fiat asset to fiat asset: for example, moving money between bank accounts.



实体资产到负债：例如信用卡还款。 / Fiat asset to liability: for example, repaying a credit card.



负债到实体资产：例如信用卡取现。 / Liability to fiat asset: for example, a credit card cash advance.



实体资产到虚拟资产：例如购买礼品卡、积分或里程。 / Fiat asset to virtual asset: for example, buying gift cards, points, or miles.



虚拟资产到虚拟资产：例如积分转换。 / Virtual asset to virtual asset: for example, converting points.

如果交易发生在建账或平账锚点之前，系统允许通过未来锚点反推之前余额。

If a transaction occurs before an account-opening or reconcile anchor, the system can infer the earlier balance backward from the future anchor.

平账 / Reconcile

平账是账户在某一天结束时的真实余额记录。平账只能从账户编辑中创建。普通流水编辑页面不能创建平账。

A reconcile record is the real account balance at the end of a specific day. Reconcile records can only be created from account editing. The regular transaction edit page cannot create reconcile records.

建账 / Account Opening

建账是新建账户时自动生成的初始平账。它用于说明账户从哪一天开始有一个已知余额。

Account opening is the initial reconcile record automatically created when a new account is created. It indicates the date from which the account has a known balance.

事件与摊销 / Events and Amortization

事件用于把多笔交易归为同一主题，例如旅行、保险、订阅或一次大型支出。

Events group multiple transactions under the same topic, such as travel, insurance, subscriptions, or a large one-time expense.

每日摊销用于统计：

Daily amortization is used for reporting:





原始流水仍只保存一笔真实金额。 / The original transaction still stores one real amount.



统计时把金额按起止日期平均分摊到每天。 / For reporting, the amount is evenly spread across each day between the start and end dates.



本周、本月、本年支出图表会使用摊销后的金额。 / Weekly, monthly, and yearly expense charts use the amortized amount.



账户余额仍按原始流水日期和金额计算，不受摊销影响。 / Account balances still use the original transaction date and amount, and are not affected by amortization.

桌面版窗口 / Desktop window size

安装版默认窗口与最小允许尺寸由 electron/window-layout.cjs 根据 src/styles.css 中的布局 token 自动汇总（当前约 1784×947 内容区像素，useContentSize，初始即最小）。宽度 = --app-min-width（1760）+ 纵向滚动条预留（24）；高度 = 页面上下内边距 + 顶栏 + max(快速记账列, 图表列)，其中快速记账按「摊销 + 事件」最长字段栈、备注最低一行（--field-row-min-height）、保存区间距逐项相加。修改 padding、表单行距或图表 min-height 后请运行 npm run layout:window 查看数值，并 npm run layout:sync-web 同步网页启动脚本。

快速记账区域不出现内部滚动条；备注区占满「保存交易」上方剩余空间，最低高度与商户行一致。网页版内容区高度建议不小于上述计算值；start-bookkeeping-web.vbs 的 Chrome 外框高度含约 130px 浏览器 UI 余量（见 BROWSER_WINDOW_HEIGHT）。

The installed app’s initial/minimum size is computed in electron/window-layout.cjs from layout tokens in src/styles.css (currently about 1784×947 content pixels with useContentSize). Width adds scrollbar gutter to --app-min-width; height sums page padding, top bar, and max(quick-entry column, charts column) with the full amortization + event form stack and one-line notes minimum. After layout changes, run npm run layout:window and npm run layout:sync-web. Quick entry does not scroll internally; notes fill space above Save. The VBS launcher uses a slightly taller outer window for Chrome UI chrome.

自动升级 / Auto Update

桌面版计划支持通过 GitHub Releases 自动升级。设置页顶部的“查看升级”按钮会在安装版中检查新版本、下载升级包并提示安装重启。

The desktop version is planned to support auto-updates through GitHub Releases. In the installed version, the "Check updates" button at the top of the settings page checks for a new version, downloads the update package, and prompts the user to install and restart.

网页版本不会执行自动升级。发布桌面升级包的具体流程见 RELEASE_UPDATES.md。

The web version does not perform auto-updates. See RELEASE_UPDATES.md for the desktop update release process. editing, export, and clearing data; it does not support data import.

核心原则：

Core principles:

- 账户余额是资产统计的基础。 / Account balances are the basis of asset statistics.
- 普通流水会影响账户余额。 / Regular transactions affect account balances.
- 平账记录是某一天结束时的余额锚点。 / A reconcile record is a balance anchor at the end of a specific day.
- 建账记录是新建账户时自动产生的初始平账。 / An account-opening record is the initial reconcile record automatically created with a new account.
- 资产历史可以基于未来或过去的平账锚点反推。 / Asset history can be inferred forward or backward from past or future reconcile anchors.
- 事件和摊销只影响统计口径，不改变原始流水金额。 / Events and amortization affect reporting only; they do not change the original transaction amount.

## 顶部导航 / Top Navigation

顶部标题显示应用名称。本地网页版本和桌面版使用同一套页面。

The top title shows the app name. The local web version and the desktop version use the same pages.

导航按钮包括：

Navigation buttons include:

- 总览：查看资产、现金流、资产变化和快速记账。 / Overview: view assets, cash flow, asset changes, and quick entry.
- 账户：创建、编辑和删除账户。 / Accounts: create, edit, and delete accounts.
- 流水：查看、过滤、编辑和删除交易流水，也可以查看事件流水。 / Transactions: view, filter, edit, and delete transaction records, and view event records.
- 设置：管理汇率、语言、分类、账户类型、商户、导出和清除数据。 / Settings: manage FX rates, language, categories, account types, vendors, export, and clearing data.

非设置页右上角显示中文/英文切换。设置页同一位置显示“查看升级”，用于未来桌面版自动升级；网页版本不会执行升级。

On non-settings pages, the top-right control switches between Chinese and English. On the settings page, the same position shows "Check updates" for future desktop auto-updates; the web version does not perform updates.

## 总览页面 / Overview Page

总览页由三列组成：资产概览、资产与支出图表、快速记账。

The overview page has three columns: asset overview, asset and expense charts, and quick entry.

### 资产概览卡片 / Asset Overview Card

资产概览展示当前账本的核心资产指标。

The asset overview shows the main asset metrics of the current ledger.

内容包括：

Contents include:

- 净资产：资产合计减去负债合计，以 USD 显示，并显示 CNY 折算值。 / Net worth: total assets minus total liabilities, shown in USD with a CNY equivalent.
- 资产合计：所有实体资产和虚拟资产的合计价值。 / Total assets: the total value of all fiat and virtual assets.
- 负债合计：所有负债账户的合计债务。 / Total liabilities: the total debt across all liability accounts.
- 法币资产：实体资产账户折算后的总额。 / Fiat assets: the converted total of fiat asset accounts.
- 虚拟资产：积分、里程、代币等虚拟资产按单价折算后的总额。 / Virtual assets: the converted value of points, miles, tokens, and other virtual assets based on unit price.

下方资产条形图展示负债、法币资产和虚拟资产在同一坐标轴上的位置。负债在零点左侧，资产在零点右侧。坐标轴数值固定保留两位小数。

The asset bar chart below places liabilities, fiat assets, and virtual assets on the same axis. Liabilities appear to the left of zero, and assets appear to the right. Axis values always keep two decimal places.

图例分两层：

The legend has two levels:

- 上层大类图例：负债、法币资产、虚拟资产。 / Top-level legend: liabilities, fiat assets, and virtual assets.
- 下层细分图例：按账户类型或自定义账户类型显示。 / Detail legend: displayed by account type or custom account type.

底部说明文字提示总览使用设置中的有效 USD/CNY 汇率。

The note at the bottom indicates that the overview uses the effective USD/CNY rate from settings.

### 资产变化卡片 / Asset Change Card

资产变化展示一段时间内的资产结构趋势。

Asset change shows the trend of asset structure over a selected period.

图表内容：

Chart contents:

- 负债：以负方向显示。 / Liabilities: shown in the negative direction.
- 法币资产：以柱状堆叠显示。 / Fiat assets: shown as stacked bars.
- 虚拟资产：以柱状堆叠显示。 / Virtual assets: shown as stacked bars.
- 净资产：以折线显示。 / Net worth: shown as a line.

时间范围按钮包括：

Time range buttons include:

- 4月 / 4 months
- 8月 / 8 months
- 1年 / 1 year
- 3年 / 3 years
- YTD / YTD
- 自选 / Custom

自选范围会显示开始和结束日期输入框。图表按半月采样，适合观察长期变化。

The custom range shows start and end date inputs. The chart samples roughly every half month, making it suitable for long-term trends.

资产历史的计算逻辑：

Asset history calculation logic:

- 如果某日之前有平账锚点，从该锚点向后累加流水。 / If there is a reconcile anchor before a day, the system starts from that anchor and adds later transactions.
- 如果某日之后有平账锚点，从未来锚点向前反推余额。 / If there is a reconcile anchor after a day, the system starts from the future anchor and infers the earlier balance backward.
- 新建账户自动有“建账”锚点，因此建账前的流水可以反推出更早余额。 / A new account automatically has an account-opening anchor, so transactions before account opening can infer earlier balances.

### 本周支出卡片 / This Week Expense Card

本周支出卡片展示本周现金流摘要和支出分类饼图。

The this-week expense card shows this week's cash flow summary and expense category pie chart.

内容包括：

Contents include:

- 收入 / Income
- 支出 / Expenses
- 净流入/净支出 / Net inflow or net outflow
- 本周支出饼图 / This-week expense pie chart
- 共享分类图例 / Shared category legend

转账和平账不会计入现金流。普通收入和支出会计入。启用每日摊销的流水会按设置的日期区间分摊到每一天，用于本周、本月、本年统计。

Transfers and reconcile records are not counted as cash flow. Regular income and expenses are counted. Transactions with daily amortization enabled are spread across the configured date range and used in weekly, monthly, and yearly statistics.

### 本月支出卡片 / This Month Expense Card

本月支出卡片展示本月支出分类饼图和本月现金流摘要。

The this-month expense card shows this month's expense category pie chart and cash flow summary.

内容包括：

Contents include:

- 本月收入 / This-month income
- 本月支出 / This-month expenses
- 本月净额 / This-month net amount
- 本月支出分类饼图 / This-month expense category pie chart

如果本月没有支出，会显示空状态提示。

If there are no expenses this month, an empty-state message is shown.

### 本年支出卡片 / This Year Expense Card

本年支出卡片展示本年支出分类饼图和本年现金流摘要。

The this-year expense card shows this year's expense category pie chart and cash flow summary.

内容包括：

Contents include:

- 本年收入 / This-year income
- 本年支出 / This-year expenses
- 本年净额 / This-year net amount
- 本年支出分类饼图 / This-year expense category pie chart

本年统计同样遵守事件摊销逻辑。

Yearly statistics also follow the event amortization logic.

### 快速记账卡片 / Quick Entry Card

快速记账用于快速新增支出、收入或转账。

Quick entry is used to quickly add expenses, income, or transfers.

支出字段包括：

Expense fields include:

- 类型 / Type
- 账户 / Account
- 日期 / Date
- 大类 / Main category
- 明细 / Detail category
- 商户 / Vendor
- 金额 / Amount
- 每日摊销 / Daily amortization
- 特定事件 / Specific event
- 备注 / Notes

收入字段包括：

Income fields include:

- 类型 / Type
- 账户 / Account
- 日期 / Date
- 大类 / Main category
- 明细 / Detail category
- 商户 / Vendor
- 金额 / Amount
- 每日摊销 / Daily amortization
- 特定事件 / Specific event
- 备注 / Notes

转账字段包括：

Transfer fields include:

- 类型 / Type
- 转出账户 / Source account
- 转入账户 / Target account
- 日期 / Date
- 金额 / Amount
- 备注 / Notes

账户下拉列表展开时按资产大类和账户类型分组。选中后只显示账户名称。转账支持：

When the account dropdown is expanded, accounts are grouped by asset group and account type. After selection, only the account name is shown. Supported transfers include:

- 实体资产到实体资产。 / Fiat asset to fiat asset.
- 实体资产到负债，用于信用卡还款。 / Fiat asset to liability, used for credit card repayment.
- 负债到实体资产，用于取现或借款入账。 / Liability to fiat asset, used for cash advance or loan proceeds.
- 实体资产或负债到虚拟资产，用于购买积分、礼品卡、里程等。 / Fiat asset or liability to virtual asset, used to buy points, gift cards, miles, and similar assets.
- 虚拟资产到虚拟资产，用于积分或里程转换。 / Virtual asset to virtual asset, used for points or miles conversion.

## 流水页面 / Transactions Page

流水页分为交易流水和事件流水两个视图。

The transactions page has two views: transaction records and event records.

### 交易流水视图 / Transaction Records View

交易流水列表展示每一笔原始交易。

The transaction list shows each original transaction.

表格列包括：

Table columns include:

- 日期 / Date
- 账户 / Account
- 类型 / Type
- 分类 / Category
- 事件 / Event
- 商户 / Vendor
- 金额 / Amount
- 操作 / Actions

账户列会显示资产大类，例如“实体资产 · Chase”。转账会显示转出与转入两侧，例如“实体资产 · Chase → 负债 · CFU”。

The account column shows the asset group, for example "Fiat assets · Chase". Transfers show both source and target sides, for example "Fiat assets · Chase → Liability · CFU".

类型包括：

Types include:

- 支出 / Expense
- 收入 / Income
- 转账 / Transfer
- 平账 / Reconcile

平账不能在流水编辑弹窗中改为普通交易。建账记录属于平账的一种，分类显示为“建账”。

A reconcile record cannot be changed into a regular transaction in the transaction edit dialog. An account-opening record is a type of reconcile record, and its category is shown as "Account opening".

筛选器包括：

Filters include:

- 类型 / Type
- 商户关键词 / Vendor keyword
- 分类大类 / Main category
- 分类明细 / Detail category
- 账户大类 / Account group
- 账户 / Account
- 开始日期 / Start date
- 结束日期 / End date

当上级筛选条件变化时，相关下级筛选会自动清空，避免选择不存在的组合。

When a parent filter changes, related child filters are cleared automatically to avoid invalid combinations.

### 编辑流水 / Editing Transactions

支出和收入流水可以编辑：

Expense and income transactions can edit:

- 账户 / Account
- 日期 / Date
- 分类 / Category
- 商户 / Vendor
- 金额 / Amount
- 摊销 / Amortization
- 事件 / Event
- 备注 / Notes

转账流水可以编辑：

Transfer transactions can edit:

- 转出账户 / Source account
- 转入账户 / Target account
- 日期 / Date
- 金额 / Amount
- 备注 / Notes

编辑会撤销旧流水对余额的影响，再应用新流水，并重新根据平账锚点计算受影响账户余额。

Editing first reverses the old transaction's balance effect, then applies the new transaction, and finally recomputes affected account balances based on reconcile anchors.

删除普通流水会移除该流水并重算账户余额。删除建账流水会触发二次确认；确认后会删除对应账户及相关流水。

Deleting a regular transaction removes the row and recomputes account balances. Deleting an account-opening transaction triggers a second confirmation; after confirmation, the related account and its related transactions are deleted.

### 事件流水视图 / Event Records View

事件流水把被标记为同一事件的交易汇总展示。

Event records summarize transactions marked as belonging to the same event.

每个事件会显示：

Each event shows:

- 事件名称 / Event name
- 事件日期范围 / Event date range
- 关联交易数量 / Number of linked transactions
- 原始总额 / Original total
- 本周摊销额 / This-week amortized amount
- 本月摊销额 / This-month amortized amount
- 本年摊销额 / This-year amortized amount

点击事件可进入事件编辑。事件用于统计归集，不直接改变账户余额。

Clicking an event opens event editing. Events are used for reporting and grouping; they do not directly change account balances.

## 账户页面 / Accounts Page

账户页面按资产大类分三列：

The accounts page is divided into three columns by asset group:

- 实体资产 / Fiat assets
- 虚拟资产 / Virtual assets
- 负债 / Liabilities

每列显示该类账户列表和合计金额。账户卡片显示：

Each column shows accounts in that group and the group total. An account card shows:

- 账户名称 / Account name
- 账户类型 / Account type
- 币种 / Currency
- 余额或数量 / Balance or quantity
- 折算值 / Converted value
- 编辑按钮 / Edit button

### 新建账户逻辑 / New Account Logic

新建账户时需要填写：

When creating an account, fill in:

- 账户名称 / Account name
- 账户大类与账户类型 / Account group and account type
- 币种 / Currency
- 初始余额 / Opening balance
- 虚拟资产单价 / Virtual asset unit price
- 负债额度 / Liability credit line
- 备注 / Notes

新建账户本身会自动生成一条“建账”平账记录。建账日期戳记为创建当日的明天。这样当你在建账日期之前补录交易时，系统可以从建账余额向前反推历史余额。

Creating an account automatically creates an "account opening" reconcile record. The account-opening date stamp is tomorrow relative to the creation date. This lets the system infer earlier balances backward from the opening balance when you add transactions before the opening date.

### 编辑账户逻辑 / Account Editing Logic

未勾选“记录为平账”时，编辑账户只修改账户资料，例如：

When "Record as reconcile" is not checked, editing an account only changes account details, such as:

- 名称 / Name
- 类型 / Type
- 币种 / Currency
- 虚拟资产单价 / Virtual asset unit price
- 信用额度 / Credit line
- 备注 / Notes

勾选“记录为平账”时，当前填写的余额会作为所选日期结束时的余额锚点。系统会创建一条平账流水，并根据该锚点重算账户余额。

When "Record as reconcile" is checked, the entered balance becomes the balance anchor at the end of the selected date. The system creates a reconcile transaction and recomputes the account balance from that anchor.

平账的作用：

The purpose of reconcile records:

- 固定某一天结束时的真实余额。 / Fix the real balance at the end of a specific day.
- 让之后的流水向后推算余额。 / Let later transactions calculate balances forward.
- 让之前的流水向前反推余额。 / Let earlier transactions infer balances backward.

### 删除账户 / Deleting Accounts

普通删除账户要求账户没有关联流水。建账记录被删除时，会二次确认并删除该账户及其相关流水。

Regular account deletion requires the account to have no linked transactions. When an account-opening record is deleted, the system asks for a second confirmation and then deletes the account and its related transactions.

## 设置页面 / Settings Page

设置页包含左侧基础设置、中间分类管理、右侧账户类型和商户管理。

The settings page contains basic settings on the left, category management in the middle, and account type plus vendor management on the right.

### 汇率卡片 / FX Rate Card

汇率卡片控制 USD/CNY 折算。

The FX rate card controls USD/CNY conversion.

内容包括：

Contents include:

- 当前有效汇率 / Current effective rate
- 最近 API 汇率 / Latest API rate
- 上次刷新时间 / Last refresh time
- 手动汇率输入框 / Manual rate input
- 保存覆盖 / Save override
- 从 Frankfurter 刷新 / Refresh from Frankfurter

如果设置了手动汇率，总览和账户折算会优先使用手动汇率。留空则使用最近 API 汇率或默认值。

If a manual rate is set, overview and account conversions use the manual rate first. If left blank, the app uses the latest API rate or the default value.

### 数据导出和清除卡片 / Data Export and Clear Card

当前版本支持：

The current version supports:

- 导出 Excel / Export Excel
- 清除全部数据 / Clear all data

导出 Excel 用于备份当前账本。清除全部数据会二次确认，并清空账户、流水、事件、商户和汇率数据。

Export Excel is used to back up the current ledger. Clear all data asks for confirmation twice and clears accounts, transactions, events, vendors, and FX data.

当前版本不支持导入数据。

The current version does not support data import.

### 地址、时区与语言卡片 / Region, Timezone, and Language Card

该卡片显示当前浏览器检测到的时区，并提供中文和英文界面切换。

This card shows the timezone detected by the browser and provides Chinese and English interface switching.

日期输入与显示按照本机浏览器区域和时区处理。

Date input and display follow the local browser region and timezone.

### 分类管理卡片 / Category Management Card

分类管理用于管理支出和收入分类。

Category management is used to manage expense and income categories.

功能包括：

Features include:

- 支出/收入切换 / Expense and income toggle
- 搜索分类 / Search categories
- 编辑模式 / Edit mode
- 新增自定义大类 / Add custom main category
- 新增自定义明细 / Add custom detail category
- 隐藏默认大类或默认明细 / Hide built-in main or detail categories
- 删除自定义大类或明细 / Delete custom main or detail categories
- 拖拽调整顺序 / Drag to reorder
- 撤销删除 / Undo deletion

默认支出分类采用当前标准分类，不支持导入旧分类。

The default expense categories use the current standard taxonomy. Old imported categories are not supported.

### 账户类型管理卡片 / Account Type Management Card

账户类型管理用于维护账户的子类型。

Account type management is used to maintain account subtypes.

功能包括：

Features include:

- 实体资产、虚拟资产、负债三类切换 / Toggle between fiat assets, virtual assets, and liabilities
- 搜索账户类型 / Search account types
- 编辑模式 / Edit mode
- 新增自定义账户类型 / Add custom account type
- 隐藏默认账户类型 / Hide built-in account type
- 删除未被账户使用的自定义账户类型 / Delete custom account types that are not used by any account
- 拖拽调整顺序 / Drag to reorder

账户列表、账户编辑、快速记账下拉和总览图例都会使用这里的账户类型名称。

The account list, account editing, quick-entry dropdown, and overview legend all use account type names from this card.

### 商户管理卡片 / Vendor Management Card

商户管理展示系统记录过的商户名称。

Vendor management shows vendor names recorded by the system.

功能包括：

Features include:

- 搜索商户 / Search vendors
- 编辑模式 / Edit mode
- 删除商户 / Delete vendors
- 撤销删除 / Undo deletion

商户用于快速记账自动补全，也用于按商户筛选流水。

Vendors are used for quick-entry autocomplete and for filtering transactions by vendor.

## 记账和余额计算逻辑 / Transaction and Balance Logic

### 支出 / Expense

支出会减少实体资产或虚拟资产余额。对于负债账户，支出会增加负债余额。

An expense reduces a fiat asset or virtual asset balance. For a liability account, an expense increases the liability balance.

### 收入 / Income

收入会增加实体资产或虚拟资产余额。对于负债账户，收入可作为还款，会减少负债余额。

Income increases a fiat asset or virtual asset balance. For a liability account, income can act as repayment and reduce the liability balance.

### 转账 / Transfer

转账不计入支出或收入统计。它只在账户之间移动余额。

Transfers are not counted as income or expenses. They only move balances between accounts.

常见转账：

Common transfers:

- 实体资产到实体资产：例如银行账户之间转钱。 / Fiat asset to fiat asset: for example, moving money between bank accounts.
- 实体资产到负债：例如信用卡还款。 / Fiat asset to liability: for example, repaying a credit card.
- 负债到实体资产：例如信用卡取现。 / Liability to fiat asset: for example, a credit card cash advance.
- 实体资产到虚拟资产：例如购买礼品卡、积分或里程。 / Fiat asset to virtual asset: for example, buying gift cards, points, or miles.
- 虚拟资产到虚拟资产：例如积分转换。 / Virtual asset to virtual asset: for example, converting points.

如果交易发生在建账或平账锚点之前，系统允许通过未来锚点反推之前余额。

If a transaction occurs before an account-opening or reconcile anchor, the system can infer the earlier balance backward from the future anchor.

### 平账 / Reconcile

平账是账户在某一天结束时的真实余额记录。平账只能从账户编辑中创建。普通流水编辑页面不能创建平账。

A reconcile record is the real account balance at the end of a specific day. Reconcile records can only be created from account editing. The regular transaction edit page cannot create reconcile records.

### 建账 / Account Opening

建账是新建账户时自动生成的初始平账。它用于说明账户从哪一天开始有一个已知余额。

Account opening is the initial reconcile record automatically created when a new account is created. It indicates the date from which the account has a known balance.

### 事件与摊销 / Events and Amortization

事件用于把多笔交易归为同一主题，例如旅行、保险、订阅或一次大型支出。

Events group multiple transactions under the same topic, such as travel, insurance, subscriptions, or a large one-time expense.

每日摊销用于统计：

Daily amortization is used for reporting:

- 原始流水仍只保存一笔真实金额。 / The original transaction still stores one real amount.
- 统计时把金额按起止日期平均分摊到每天。 / For reporting, the amount is evenly spread across each day between the start and end dates.
- 本周、本月、本年支出图表会使用摊销后的金额。 / Weekly, monthly, and yearly expense charts use the amortized amount.
- 账户余额仍按原始流水日期和金额计算，不受摊销影响。 / Account balances still use the original transaction date and amount, and are not affected by amortization.

## 自动升级 / Auto Update

桌面版计划支持通过 GitHub Releases 自动升级。设置页顶部的“查看升级”按钮会在安装版中检查新版本、下载升级包并提示安装重启。

The desktop version is planned to support auto-updates through GitHub Releases. In the installed version, the "Check updates" button at the top of the settings page checks for a new version, downloads the update package, and prompts the user to install and restart.

网页版本不会执行自动升级。发布桌面升级包的具体流程见 `RELEASE_UPDATES.md`。

The web version does not perform auto-updates. See `RELEASE_UPDATES.md` for the desktop update release process.
