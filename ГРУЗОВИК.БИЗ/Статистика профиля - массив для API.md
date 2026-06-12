```
const userStatisticMock = {  
  
    // Вкладка-1 - Сводка  
    kpi: [  
        { 
        key: 'impressions', 
        value: '142567', 
        change: '+12.5%', 
        isPositive: true 
        },  
        { key: 'ctr', value: '2,1', change: '+0.3%', isPositive: true, suffix: '%' },  
        { key: 'views', value: '2994', change: '+8.7%', isPositive: true },  
        { key: 'targetActions', value: '142', change: '+22.1%', isPositive: true },  
        { key: 'contacts', value: '287', change: '+15.2%', isPositive: true },  
    ],  
  
    // распределение целевых действий  
    actionsDistribution: [  
        {  
            key: 'phoneview',  
            value: 84,  
        },  
        {  
            key: 'callrequests',  
            value: 37,  
        },  
        {  
            key: 'chatopened',  
            value: 18,  
        },  
        {  
            key: 'favoriteadded',  
            value: 12,  
        },  
    ],  
  
    // воронка  
    funnelChart: [  
            {stage: 'Показы', number: 1000},  
            {stage: 'Просмотры', number: 500},  
            {stage: 'Целевое действие', number: 200},  
            {stage: 'Контакты', number: 80},  
        ],  
    
  
  
    // топ по просмотрам  
    topMetricsViewsTable: {  
        columns: [  
            {title: 'Модель'},  
            {title: 'Просмотры', unit: ''},  
        ],  
        rows: [  
            ['КамАЗ 6520 самосвал', '1247'],  
            ['МАЗ 6312 тягач', '891'],  
            ['Вакуумная МВ-11', '803'],  
            ['Полуприцеп KOINE', '631'],  
            ['Самосвал НЕФАЗ', '587'],  
            ['КамАЗ 43118 шасси', '580'],  
            ['Тягач МАЗ 5440', '570'],  
            ['Полуприцеп бортовой', '437'],  
        ]  
    },  
  
    // топ по ctr  
    topMetricsCtrTable: {  
        columns: [  
            {title: 'Модель'},  
            {title: 'CTR', unit: '%'},  
        ],  
        rows: [  
            ['Вакуумная МВ-11', '4.7'],  
            ['КамАЗ 6520', '3.2'],  
            ['КамАЗ 43118', '3.1'],  
            ['Вакуумная МВ-10', '2.9'],  
            ['Самосвал НЕФАЗ', '2.8'],  
            ['Полуприцеп KOINE', '2.7'],  
            ['Тягач МАЗ 5440', '2.6'],  
            ['Самосвал НЕФАЗ', '2.8'],  
        ]  
    },  
  
    // топ по целевым действиям  
    topMetricsActionsTable: {  
        columns: [  
            {},  
            {unit: ' шт.'},  
        ],  
        rows: [  
            ['КамАЗ 6520', '42'],  
            ['Вакуумная МВ-11', '31'],  
            ['МАЗ 6312', '23'],  
            ['КамАЗ 43118', '21'],  
            ['Самосвал НЕФАЗ', '20'],  
            ['Полуприцеп KOINE', '19'],  
            ['Тягач МАЗ 5440', '18'],  
            ['КамАЗ 43118', '21'],  
        ]  
    },  
  
    // график - динамика просмотров  
    viewsDynamicChart: [  
        {label: '01.09', value: 245},  
        {label: '02.09', value: 278},  
        {label: '03.09', value: 221},  
        {label: '04.09', value: 310},  
        {label: '05.09', value: 265},  
        {label: '06.09', value: 232},  
        {label: '07.09', value: 289},  
        {label: '08.09', value: 254},  
        {label: '09.09', value: 301},  
        {label: '10.09', value: 275},  
    ],  
  
    // график - динамика целевых действий  
    actionsDynamicChart: [  
        {label: '01.09', value: 245},  
        {label: '02.09', value: 278},  
        {label: '03.09', value: 221},  
        {label: '04.09', value: 310},  
        {label: '05.09', value: 265},  
        {label: '06.09', value: 232},  
        {label: '07.09', value: 289},  
        {label: '08.09', value: 254},  
        {label: '09.09', value: 301},  
        {label: '10.09', value: 275},  
    ],  
  
    // график - динамика по ctr  
    ctrDynamicChart: [  
        {label: '01.09', value: 245},  
        {label: '02.09', value: 278},  
        {label: '03.09', value: 221},  
        {label: '04.09', value: 310},  
        {label: '05.09', value: 265},  
        {label: '06.09', value: 232},  
        {label: '07.09', value: 289},  
        {label: '08.09', value: 254},  
        {label: '09.09', value: 301},  
        {label: '10.09', value: 275},  
    ],  
  
    // Вкладка 2 - Детализация  
    // график - детализированная аналитика    detailedAnalyticsChart: [  
        {label: '01.09', value: 245},  
        {label: '02.09', value: 278},  
        {label: '03.09', value: 221},  
        {label: '04.09', value: 310},  
        {label: '05.09', value: 265},  
        {label: '06.09', value: 232},  
        {label: '07.09', value: 289},  
        {label: '08.09', value: 254},  
        {label: '09.09', value: 301},  
        {label: '10.09', value: 275},  
    ],  
  
    // таблица - детализированная статистика  
    groupAnalyzeTable: {  
        columns: [  
            { title: 'Тип' },  
            { title: 'Сумма', align: 'right' },  
            { title: 'Доля', align: 'right' },  
            { title: 'CPV', align: 'right' },  
            { title: 'CPL', align: 'right' },  
            { title: 'CPA', align: 'right' },  
        ],  
        rows: [  
            ['Выведение', '8,500 ₽', '45.3%', '12.8 ₽', '158 ₽', '312 ₽'],  
            ['ТОП', '6,250 ₽', '33.3%', '18.4 ₽', '180 ₽', '370 ₽'],  
            ['PRO', '4,000 ₽', '21.4%', '21.1 ₽', '201 ₽', '402 ₽'],  
            ['Итого', '18,750 ₽', '100%', '16.8 ₽', '178 ₽', '356 ₽'],  
        ]  
    },  
  
  
    // Вкладка 4 - Целевые действия  
    actionsHistoryTable: {  
        columns: [  
            {title: 'Дата'},  
            {title: 'Объявление', align: 'left'},  
            {title: 'Тип', align: 'left'},  
            {title: 'Источник', align: 'left'},  
            {title: 'Регион', align: 'left'},  
            {title: 'Устройство', align: 'left'},  
        ],  
        rows: [  
            ['15.08.2025 15:45', 'КамАЗ 6520 самосвал', 'Просмотр телефона', 'Поиск', 'Москва', 'Desktop'],  
            ['15.08.2025 14:22', 'МАЗ 6312 тягач', 'Чат', 'Каталог', 'СПб', 'Mobile'],  
            ['14.08.2025 21:45', 'Полуприцеп KRONE', 'Запрос КП', 'Поиск', 'Екатеринбург', 'Mobile'],  
            ['14.08.2025 20:15', 'Вакуумник МВ-11', 'Просмотр телефона', 'Поиск', 'Казань', 'Desktop'],  
            ['14.08.2025 19:45', 'Самосвал НЕФАЗ', 'Просмотр телефона', 'Поиск', 'Тюмень', 'Desktop'],  
            ['14.08.2025 19:15', 'КамАЗ 4118 шасси', 'Чат', 'Каталог', 'Челябинск', 'Mobile'],  
            ['14.08.2025 17:45', 'Тягач МАЗ 5440', 'Запрос КП', 'Поиск', 'Ростов-на-Дону', 'Desktop'],  
            ['13.08.2025 12:59', 'Полуприцеп бортовой', 'Чат', 'Каталог', 'Краснодар', 'Mobile'],  
            ['13.08.2025 12:45', 'КамАЗ 65115', 'Просмотр телефона', 'Поиск', 'Уфа', 'Desktop'],  
        ]  
    },  
  
  
};
```


**API**

**Вкладка 1: Сводка**

**GET** **`/api/user-statistic/summary?from=225-09-19&to=2025-09-30`**

Возвращает:
- `kpi[]`
- `actionsDistribution[]`
- `funnelChart`
- `topMetricsViewsTable`
- `topMetricsCtrTable`
- `topMetricsActionsTable`
- `viewsDynamicChart[]`
- `actionsDynamicChart[]`
- `ctrDynamicChart[]`


**Вкладка 2: Детализация**

**GET `/api/user-statistic/details`** 

Возвращает:
- `detailedAnalyticsChart[]`
- `groupAnalyzeTable`


**Вкладка 3: Целевые действия**
**GET** `/api/user-statistic/actions`
Возвращает:
- `actionsHistoryTable`			
		- { name: 'КамАЗ 43118', value: 21 },  
			{ name: 'Самосвал НЕФАЗ', value: 20 },  
			{ name: 'Полуприцеп KOINE', value: 19 },  
			{ name: 'Тягач МАЗ 5440', value: 18 },  
			{ name: 'КамАЗ 43118', value: 21 },  
		]  
	}  
},  

viewsDynamicChart: Array.from({ length: 30 }, (_, i) => ({  
	label: `${String(i + 1).padStart(2, '0')}.09`,  
	value: Math.floor(200 + Math.random() * 100),  
})),  

actionsDynamicChart: Array.from({ length: 30 }, (_, i) => ({  
	label: `${String(i + 1).padStart(2, '0')}.09`,  
	value: Math.floor(20 + Math.random() * 15),  
})),  

ctrDynamicChart: Array.from({ length: 30 }, (_, i) => ({  
	label: `${String(i + 1).padStart(2, '0')}.09`,  
	value: +(2 + Math.random() * 2).toFixed(1),  
})),  

// Вкладка 4 - Целевые действия  
actionsHistoryTable : {  
	columns: [  
		{title: 'Дата'},  
		{title: 'Объявление', align: 'left'},  
		{title: 'Тип', align: 'left'},  
		{title: 'Источник', align: 'left'},  
		{title: 'Регион', align: 'left'},  
		{title: 'Устройство', align: 'left'},  
	],  
	rows: [  
		{  
			name: '15.08.2025 15:45',  
			value1: 'КамАЗ 6520 самосвал',  
			value2: 'Просмотр телефона',  
			value3: 'Поиск',  
			value4: 'Москва',  
			value5: 'Desktop',  
		},  
		{  
			name: '15.08.2025 14:22',  
			value1: 'МАЗ 6312 тягач',  
			value2: 'Чат',  
			value3: 'Каталог',  
			value4: 'СПб',  
			value5: 'Mobile',  
		},  
		{  
			name: '14.08.2025 21:45',  
			value1: 'Полуприцеп KRONE',  
			value2: 'Запрос КП',  
			value3: 'Поиск',  
			value4: 'Екатеринбург',  
			value5: 'Mobile',  
		},  
		{  
			name: '14.08.2025 20:15',  
			value1: 'Вакуумник МВ-11',  
			value2: 'Просмотр телефона',  
			value3: 'Поиск',  
			value4: 'Казань',  
			value5: 'Desktop',  
		},  
		{  
			name: '14.08.2025 19:45',  
			value1: 'Самосвал НЕФАЗ',  
			value2: 'Просмотр телефона',  
			value3: 'Поиск',  
			value4: 'Тюмень',  
			value5: 'Desktop',  
		},  
		{  
			name: '14.08.2025 19:15',  
			value1: 'КамАЗ 4118 шасси',  
			value2: 'Чат',  
			value3: 'Каталог',  
			value4: 'Челябинск',  
			value5: 'Mobile',  
		},  
		{  
			name: '14.08.2025 17:45',  
			value1: 'Тягач МАЗ 5440',  
			value2: 'Запрос КП',  
			value3: 'Поиск',  
			value4: 'Ростов-на-Дону',  
			value5: 'Desktop',  
		},  
		{  
			name: '13.08.2025 12:59',  
			value1: 'Полуприцеп бортовой',  
			value2: 'Чат',  
			value3: 'Каталог',  
			value4: 'Краснодар',  
			value5: 'Mobile',  
		},  
		{  
			name: '13.08.2025 12:45',  
			value1: 'КамАЗ 65115',  
			value2: 'Просмотр телефона',  
			value3: 'Поиск',  
			value4: 'Уфа',  
			value5: 'Desktop',  
		}  
	]  
},  
  

```


1. KPI, ТОП, графики
2. Постраничный вывод: Детализация: просмотры, показы, контакты, ctr
3. Постраничный вывод: Целевые действия

- **GET /api/v1/statistic/summary**   
- **GET /api/v1/statistic/kpiStat**
- **GET /api/v1/statistic/targetActionsLog**




1. **GET /api/v1/statistic/summary**   

| Параметр | Тип  | Обязательный | Описание                                      |
| -------- | ---- | ------------ | --------------------------------------------- |
| from     | date | Да           | Начальная дата периода (в формате YYYY-MM-DD) |
| to       | date | Да           | Конечная дата периода (в формате YYYY-MM-DD)  |
Пример запроса: *GET /api/v1/statistic/summary?from=2025-08-01&to=2025-08-30

Пример ответа:

{
	"error": "Текст ошибки",
	"result": {
	"kpi": {
		  "impressions": { "value": 142567, "change": 12.5, "isPositive": true },
		  "ctr":        { "value": 2.1,     "change": 0.3,  "isPositive": true },
		  "views":      { "value": 2994,    "change": 8.7,  "isPositive": true },
		  "targetActions": { "value": 142,  "change": 22.1, "isPositive": true },
		  "contactInitiated": { "value": 287, "change": 15.2, "isPositive": true },
		  "phoneView":  { "value": 84 },
		  "callRequest":{ "value": 37 },
		  "chatMessage":{ "value": 18 },
		  "favoriteAdded": { "value": 12 }
		},
		
	"top": {
		"topCtr": [
			{
				"adv": {
					"id": 250153,
					"title": "КамАЗ 6520 самосвал",
					"url": "https://gruzovik.biz/ekaterinburg/item/225198-shtabeler-toyota-forklift-7fbr15",
					"image": "https://gruzovik.biz/sites/default/files/styles/inpf/public/unit_technic/431281019_richtrak-elektro-shtabeler.jpg?itok=o4RiqaBA",
					}
				"ctr": 0.5
			},
			...	
		],
	
		"topViews": [
			{
				"adv": {
					"id": 250153,
					"title": "КамАЗ 6520 самосвал",
					"url": "https://gruzovik.biz/ekaterinburg/item/225198-shtabeler-toyota-forklift-7fbr15",
					"image": "https://gruzovik.biz/sites/default/files/styles/inpf/public/unit_technic/431281019_richtrak-elektro-shtabeler.jpg?itok=o4RiqaBA",
					}
				"views": 1247
			},
			...	
		],
		
		"topTargetActions": [
			{
				"adv": {
					"id": 250153,
					"title": "КамАЗ 6520 самосвал",
					"url": "https://gruzovik.biz/ekaterinburg/item/225198-shtabeler-toyota-forklift-7fbr15",
					"image": "https://gruzovik.biz/sites/default/files/styles/inpf/public/unit_technic/431281019_richtrak-elektro-shtabeler.jpg?itok=o4RiqaBA",
					}
				"targetActions": 16
			},
			...	
		],
		
	},
	
	"timeline": [
		{
				"date": "2025-08-01",
				"metrics": {
					"impressions": 500,
					"views": 310,
					"targetActions": 20,
					"contactInitiated": 5,
					"ctr": 6.5,
					"cr": 4.8,
					"phoneView": 2,
					"callRequest": 3,
					"chatMessage": 1,
					"favoriteAdded": 3,
				}
			  },
			  {
				"date": "2025-08-02",
				"metrics": {
					"impressions": 500,
					"views": 310,
					"targetActions": 20,
					"contactInitiated": 5,
					"ctr": 6.5,
					"cr": 4.8,
					"phoneView": 2,
					"callRequest": 3,
					"chatMessage": 1,
					"favoriteAdded": 3,
				}
			  },
			  ...
		]
	}
}




2. **GET /api/v1/statistic/kpiStat**

| Параметр  | Тип     | Обязательный | Описание                                                        |
| --------- | ------- | ------------ | --------------------------------------------------------------- |
| from      | date    | Да           | Начальная дата периода (в формате YYYY-MM-DD)                 |
| to        | date    | Да           | Конечная дата периода (в формате YYYY-MM-DD)                  |
| perPage   | integer | Нет          | Количество выводимых объявлений на странице (по умолчанию 10) |
| page      | integer | Нет          | Текущая страница (по умолчанию 1)                             |
| sortBy    | string  | Нет          | Сортировка по полю (по умолчанию views)                       |
| sortOrder | string  | Нет          | Направление сортировки (по умолчанию desc)                    |
| limit     | integer | Нет          | Ограничение результатов (по умолчанию 1000)                     |
Пример запроса: *GET /api/v1/statistic/kpiStat?from=2025-08-01&to=2025-08-30&perPage=10&page=2&sortBy=views&sortOrder=desc

Пример ответа:

`{`
	`error: "Текст ошибки",`
	`result: {`
			`"total": 3247,`
			`"page": 1,`
			`"sortBy": "views",`
			`"sortOrder": "desc",`
			`"limit": 1000`,
			
			"items": [
				{
					"adv": {
						"id": 250153,
						"title": "КамАЗ 6520 самосвал",
						"url": "https://gruzovik.biz/ekaterinburg/item/225198-shtabeler-toyota-forklift-7fbr15",
						"image": "https://gruzovik.biz/sites/default/files/styles/inpf/public/unit_technic/431281019_richtrak-elektro-shtabeler.jpg?itok=o4RiqaBA",
						},
						
					"impressions": 500,
					"views": 310,
					"targetActions": 20,
					"contactInitiated": 5,
					"ctr": 6.5,
					"cr": 4.8,
					"phoneView": 2,
					"callRequest": 3,
					"chatMessage": 1,
					"favoriteAdded": 3,
					"position": "#1"
				},
				...
				{}
			]
		`}`
}




3.  **GET /api/v1/statistic/targetActionsLog

| Параметр  | Тип     | Обязательный | Описание                                                      |
| --------- | ------- | ------------ | ------------------------------------------------------------- |
| from      | date    | Да           | Начальная дата периода (в формате YYYY-MM-DD)                 |
| to        | date    | Да           | Конечная дата периода (в формате YYYY-MM-DD)                  |
| perPage   | integer | Нет          | Количество выводимых объявлений на странице (по умолчанию 10) |
| page      | integer | Нет          | Текущая страница (по умолчанию 1)                             |
| sortBy    | string  | Нет          | Сортировка по полю (по умолчанию views)                       |
| sortOrder | string  | Нет          | Направление сортировки (по умолчанию desc)                    |
| limit     | integer | Нет          | Ограничение результатов (по умолчанию 1000)                   |
Пример запроса: *GET /api/v1/statistic/targetActionsLog?from=2025-08-01&to=2025-08-30&perPage=10&page=2&sortBy=views&sortOrder=desc

Пример ответа:

`{`
	`"error": "Текст ошибки",`
	`"result": {`
		`"total": 3247,`
		`"page": 1,`
		`"sortBy": "views",`
		`"sortOrder": "desc",`
		`"limit": 1000`,
		
		"items": [
			{
				"adv": {
					"id": 250153,
					"title": "КамАЗ 6520 самосвал",
					"url": "https://gruzovik.biz/ekaterinburg/item/225198-shtabeler-toyota-forklift-7fbr15",
					"image": "https://gruzovik.biz/sites/default/files/styles/inpf/public/unit_technic/431281019_richtrak-elektro-shtabeler.jpg?itok=o4RiqaBA",
				},
	
				"date": "15.08.2025 15:45",
				"type": "Просмотр телефона",
				"source": "Поиск",
				"region": "Москва",
				"device": "Desktop"
			},
			...
			{}
		]
	}
}











ПОЛНЫЙ КОД (для мок сервера):

{
  "error": null,
  "result": {
	"kpi": {
		  "impressions": { "value": 142567, "change": 12.5},
		  "ctr":        { "value": 2.1,     "change": 0.3},
		  "views":      { "value": 2994,    "change": -8.7},
		  "targetActions": { "value": 142,  "change": 22.1},
		  "contactInitiated": { "value": 287, "change": 15.2},
		  "phoneView":  { "value": 84 },
		  "callRequest":{ "value": 37 },
		  "chatMessage":{ "value": 18 },
		  "favoriteAdded": { "value": 12 }
		},
    "top": {
      "topCtr": [
        { "adv": { "id": 1, "title": "МАЗ 5440", "url": "...", "image": "..." }, "ctr": 3.2 },
        { "adv": { "id": 2, "title": "КамАЗ 6520", "url": "...", "image": "..." }, "ctr": 2.9 },
        { "adv": { "id": 3, "title": "НЕФАЗ самосвал", "url": "...", "image": "..." }, "ctr": 2.7 },
        { "adv": { "id": 4, "title": "Полуприцеп KRONE", "url": "...", "image": "..." }, "ctr": 2.5 },
        { "adv": { "id": 5, "title": "МАЗ 6312", "url": "...", "image": "..." }, "ctr": 2.3 },
        { "adv": { "id": 6, "title": "Вакуумная МВ-11", "url": "...", "image": "..." }, "ctr": 2.1 },
        { "adv": { "id": 7, "title": "КамАЗ 6038", "url": "...", "image": "..." }, "ctr": 1.9 },
        { "adv": { "id": 8, "title": "МАЗ 4318", "url": "...", "image": "..." }, "ctr": 1.7 },
        { "adv": { "id": 9, "title": "Полуприцеп бортовой", "url": "...", "image": "..." }, "ctr": 1.5 },
        { "adv": { "id": 10, "title": "КамАЗ 65115", "url": "...", "image": "..." }, "ctr": 1.3 }
      ],
      "topViews": [
        { "adv": { "id": 1, "title": "КамАЗ 6520", "url": "...", "image": "..." }, "views": 1247 },
        { "adv": { "id": 2, "title": "МАЗ 6312", "url": "...", "image": "..." }, "views": 1180 },
        { "adv": { "id": 3, "title": "Полуприцеп KRONE", "url": "...", "image": "..." }, "views": 1102 },
        { "adv": { "id": 4, "title": "НЕФАЗ самосвал", "url": "...", "image": "..." }, "views": 1043 },
        { "adv": { "id": 5, "title": "МАЗ 5440", "url": "...", "image": "..." }, "views": 987 },
        { "adv": { "id": 6, "title": "Вакуумная МВ-11", "url": "...", "image": "..." }, "views": 921 },
        { "adv": { "id": 7, "title": "МАЗ 4318", "url": "...", "image": "..." }, "views": 874 },
        { "adv": { "id": 8, "title": "КамАЗ 6038", "url": "...", "image": "..." }, "views": 832 },
        { "adv": { "id": 9, "title": "Полуприцеп бортовой", "url": "...", "image": "..." }, "views": 799 },
        { "adv": { "id": 10, "title": "КамАЗ 65115", "url": "...", "image": "..." }, "views": 765 }
      ],
      "topTargetActions": [
        { "adv": { "id": 1, "title": "МАЗ 5440", "url": "...", "image": "..." }, "targetActions": 32 },
        { "adv": { "id": 2, "title": "КамАЗ 6520", "url": "...", "image": "..." }, "targetActions": 28 },
        { "adv": { "id": 3, "title": "НЕФАЗ самосвал", "url": "...", "image": "..." }, "targetActions": 25 },
        { "adv": { "id": 4, "title": "Полуприцеп KRONE", "url": "...", "image": "..." }, "targetActions": 22 },
        { "adv": { "id": 5, "title": "МАЗ 6312", "url": "...", "image": "..." }, "targetActions": 20 },
        { "adv": { "id": 6, "title": "Вакуумная МВ-11", "url": "...", "image": "..." }, "targetActions": 18 },
        { "adv": { "id": 7, "title": "КамАЗ 6038", "url": "...", "image": "..." }, "targetActions": 16 },
        { "adv": { "id": 8, "title": "МАЗ 4318", "url": "...", "image": "..." }, "targetActions": 14 },
        { "adv": { "id": 9, "title": "Полуприцеп бортовой", "url": "...", "image": "..." }, "targetActions": 12 },
        { "adv": { "id": 10, "title": "КамАЗ 65115", "url": "...", "image": "..." }, "targetActions": 10 }
      ]
    },
    "timeline": [
  { "date": "2025-08-01", "metrics": { "impressions": 500, "views": 310, "targetActions": 20, "contactInitiated": 5, "ctr": 6.2, "cr": 4.8, "phoneView": 2, "callRequest": 3, "chatMessage": 1, "favoriteAdded": 3 } },
  { "date": "2025-08-02", "metrics": { "impressions": 520, "views": 330, "targetActions": 22, "contactInitiated": 6, "ctr": 6.3, "cr": 4.5, "phoneView": 3, "callRequest": 2, "chatMessage": 2, "favoriteAdded": 4 } },
  { "date": "2025-08-03", "metrics": { "impressions": 480, "views": 295, "targetActions": 18, "contactInitiated": 4, "ctr": 6.1, "cr": 4.2, "phoneView": 1, "callRequest": 2, "chatMessage": 1, "favoriteAdded": 2 } },
  { "date": "2025-08-04", "metrics": { "impressions": 510, "views": 320, "targetActions": 21, "contactInitiated": 5, "ctr": 6.4, "cr": 4.6, "phoneView": 2, "callRequest": 3, "chatMessage": 2, "favoriteAdded": 3 } },
  { "date": "2025-08-05", "metrics": { "impressions": 530, "views": 340, "targetActions": 23, "contactInitiated": 6, "ctr": 6.5, "cr": 4.7, "phoneView": 3, "callRequest": 2, "chatMessage": 2, "favoriteAdded": 4 } },
  { "date": "2025-08-06", "metrics": { "impressions": 490, "views": 305, "targetActions": 19, "contactInitiated": 4, "ctr": 6.2, "cr": 4.3, "phoneView": 2, "callRequest": 2, "chatMessage": 1, "favoriteAdded": 3 } },
  { "date": "2025-08-07", "metrics": { "impressions": 515, "views": 325, "targetActions": 20, "contactInitiated": 5, "ctr": 6.3, "cr": 4.4, "phoneView": 2, "callRequest": 3, "chatMessage": 2, "favoriteAdded": 3 } },
  { "date": "2025-08-08", "metrics": { "impressions": 540, "views": 355, "targetActions": 24, "contactInitiated": 6, "ctr": 6.6, "cr": 4.8, "phoneView": 3, "callRequest": 2, "chatMessage": 2, "favoriteAdded": 4 } },
  { "date": "2025-08-09", "metrics": { "impressions": 470, "views": 290, "targetActions": 17, "contactInitiated": 4, "ctr": 6.0, "cr": 4.1, "phoneView": 1, "callRequest": 2, "chatMessage": 1, "favoriteAdded": 2 } },
  { "date": "2025-08-10", "metrics": { "impressions": 500, "views": 310, "targetActions": 20, "contactInitiated": 5, "ctr": 6.2, "cr": 4.3, "phoneView": 2, "callRequest": 3, "chatMessage": 2, "favoriteAdded": 3 } },
  { "date": "2025-08-11", "metrics": { "impressions": 525, "views": 335, "targetActions": 22, "contactInitiated": 6, "ctr": 6.4, "cr": 4.5, "phoneView": 3, "callRequest": 2, "chatMessage": 2, "favoriteAdded": 4 } },
  { "date": "2025-08-12", "metrics": { "impressions": 495, "views": 310, "targetActions": 19, "contactInitiated": 4, "ctr": 6.1, "cr": 4.2, "phoneView": 2, "callRequest": 2, "chatMessage": 1, "favoriteAdded": 3 } },
  { "date": "2025-08-13", "metrics": { "impressions": 510, "views": 320, "targetActions": 21, "contactInitiated": 5, "ctr": 6.3, "cr": 4.4, "phoneView": 2, "callRequest": 3, "chatMessage": 2, "favoriteAdded": 3 } },
  { "date": "2025-08-14", "metrics": { "impressions": 530, "views": 345, "targetActions": 23, "contactInitiated": 6, "ctr": 6.5, "cr": 4.6, "phoneView": 3, "callRequest": 2, "chatMessage": 2, "favoriteAdded": 4 } },
  { "date": "2025-08-15", "metrics": { "impressions": 480, "views": 300, "targetActions": 18, "contactInitiated": 4, "ctr": 6.0, "cr": 4.1, "phoneView": 1, "callRequest": 2, "chatMessage": 1, "favoriteAdded": 2 } },
  { "date": "2025-08-16", "metrics": { "impressions": 505, "views": 315, "targetActions": 20, "contactInitiated": 5, "ctr": 6.2, "cr": 4.3, "phoneView": 2, "callRequest": 3, "chatMessage": 2, "favoriteAdded": 3 } },
  { "date": "2025-08-17", "metrics": { "impressions": 520, "views": 330, "targetActions": 22, "contactInitiated": 6, "ctr": 6.3, "cr": 4.5, "phoneView": 3, "callRequest": 2, "chatMessage": 2, "favoriteAdded": 4 } },
  { "date": "2025-08-18", "metrics": { "impressions": 490, "views": 305, "targetActions": 19, "contactInitiated": 4, "ctr": 6.1, "cr": 4.2, "phoneView": 2, "callRequest": 2, "chatMessage": 1, "favoriteAdded": 3 } },
  { "date": "2025-08-19", "metrics": { "impressions": 515, "views": 325, "targetActions": 21, "contactInitiated": 5, "ctr": 6.3, "cr": 4.4, "phoneView": 2, "callRequest": 3, "chatMessage": 2, "favoriteAdded": 3 } },
  { "date": "2025-08-20", "metrics": { "impressions": 540, "views": 355, "targetActions": 24, "contactInitiated": 6, "ctr": 6.6, "cr": 4.8, "phoneView": 3, "callRequest": 2, "chatMessage": 2, "favoriteAdded": 4 } },
  { "date": "2025-08-21", "metrics": { "impressions": 470, "views": 290, "targetActions": 17, "contactInitiated": 4, "ctr": 6.0, "cr": 4.1, "phoneView": 1, "callRequest": 2, "chatMessage": 1, "favoriteAdded": 2 } },
  { "date": "2025-08-22", "metrics": { "impressions": 500, "views": 310, "targetActions": 20, "contactInitiated": 5, "ctr": 6.2, "cr": 4.3, "phoneView": 2, "callRequest": 3, "chatMessage": 2, "favoriteAdded": 3 } },
  { "date": "2025-08-23", "metrics": { "impressions": 510, "views": 320, "targetActions": 21, "contactInitiated": 5, "ctr": 6.4, "cr": 4.6, "phoneView": 2, "callRequest": 3, "chatMessage": 2, "favoriteAdded": 3 } },
  { "date": "2025-08-24", "metrics": { "impressions": 530, "views": 340, "targetActions": 23, "contactInitiated": 6, "ctr": 6.5, "cr": 4.7, "phoneView": 3, "callRequest": 2, "chatMessage": 2, "favoriteAdded": 4 } },
  { "date": "2025-08-25", "metrics": { "impressions": 490, "views": 305, "targetActions": 19, "contactInitiated": 4, "ctr": 6.2, "cr": 4.3, "phoneView": 2, "callRequest": 2, "chatMessage": 1, "favoriteAdded": 3 } },
  { "date": "2025-08-26", "metrics": { "impressions": 515, "views": 325, "targetActions": 20, "contactInitiated": 5, "ctr": 6.3, "cr": 4.4, "phoneView": 2, "callRequest": 3, "chatMessage": 2, "favoriteAdded": 3 } },
  { "date": "2025-08-27", "metrics": { "impressions": 540, "views": 355, "targetActions": 24, "contactInitiated": 6, "ctr": 6.6, "cr": 4.8, "phoneView": 3, "callRequest": 2, "chatMessage": 2, "favoriteAdded": 4 } },
  { "date": "2025-08-28", "metrics": { "impressions": 470, "views": 290, "targetActions": 17, "contactInitiated": 4, "ctr": 6.0, "cr": 4.1, "phoneView": 1, "callRequest": 2, "chatMessage": 1, "favoriteAdded": 2 } },
  { "date": "2025-08-29", "metrics": { "impressions": 500, "views": 310, "targetActions": 20, "contactInitiated": 5, "ctr": 6.2, "cr": 4.3, "phoneView": 2, "callRequest": 3, "chatMessage": 2, "favoriteAdded": 3 } },
  { "date": "2025-08-30", "metrics": { "impressions": 525, "views": 335, "targetActions": 22, "contactInitiated": 6, "ctr": 6.4, "cr": 4.5, "phoneView": 3, "callRequest": 2, "chatMessage": 2, "favoriteAdded": 4 } },
  { "date": "2025-08-31", "metrics": { "impressions": 490, "views": 305, "targetActions": 19, "contactInitiated": 4, "ctr": 6.2, "cr": 4.3, "phoneView": 2, "callRequest": 2, "chatMessage": 1, "favoriteAdded": 3 } }
   ]
  }
}