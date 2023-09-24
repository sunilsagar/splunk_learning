# Sample splunk queries

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase (status>400 AND status<500)
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 |fields bytes,categoryId,clientip
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=*
|fields bytes,categoryId,clientip
|table clientip,bytes,categoryId
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=*
|fields bytes,categoryId,clientip
|table clientip,bytes,categoryId
|rename categoryId AS product_name
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=*
|fields bytes,categoryId,clientip
|table clientip,bytes,categoryId
|sort bytes DESC
|rename categoryId AS product_name
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=*
|fields bytes,categoryId,clientip
|dedup categoryId
|table categoryId
|rename categoryId AS product_category
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=*
|fields bytes,categoryId,clientip
|stats count by categoryId
|rename categoryId AS product_category
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=*
|fields bytes,categoryId,clientip
|stats count by categoryId
|sort count DESC
|rename categoryId AS product_category
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* clientip=74.*
|fields bytes,categoryId,clientip
|stats count by clientip
|sort count DESC
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|stats count by clientip,categoryId
|sort count DESC
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|stats values(categoryId) as categoryId count by clientip
|sort count DESC
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* clientip=74.*
|fields bytes,categoryId,clientip
|stats count by clientip
|sort count DESC
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|stats count by clientip,categoryId
|sort count DESC
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|stats values(categoryId) as categoryId count by clientip
|sort count DESC
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|top limit=1 categoryId showperc=false
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|rare limit=3 categoryId showperc=false
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|timechart count by categoryId
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|rare limit=3 categoryId showperc=false
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=* categoryId=* 
|fields bytes,categoryId,clientip
| eval error = if(status == 200, "OK", "Problem")
|stats values(status) count by error
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=* categoryId=* 
|fields bytes,categoryId,clientip
| stats sum(bytes) by clientip
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|top limit=1 categoryId showperc=false
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|rare limit=3 categoryId showperc=false
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|timechart count by categoryId
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|rare limit=3 categoryId showperc=false
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=* categoryId=* 
|fields bytes,categoryId,clientip
| eval error = if(status == 200, "OK", "Problem")
|stats values(status) count by error
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=* categoryId=* 
|fields bytes,categoryId,clientip
| stats sum(bytes) by clientip
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|rare limit=3 categoryId showperc=false
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|timechart count by categoryId
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=200 categoryId=* 
|fields bytes,categoryId,clientip
|rare limit=3 categoryId showperc=false
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=* categoryId=* 
|fields bytes,categoryId,clientip
| eval error = if(status == 200, "OK", "Problem")
|stats values(status) count by error
```

```bash
index="sunil"  sourcetype="access_combined_wcookie" action=PurcHase status=* categoryId=* 
|fields bytes,categoryId,clientip
| stats sum(bytes) by clientip
```