импорт необходимых пакетов
import pandas as pd
import pandas_profiling
df = pd.read_csv('titanic/train.csv')
pandas_profiling.ProfileReport(df)
экспортируем в интерактивный HTML-файл 
profile = pandas_profiling.ProfileReport(df)
profile.to_file(outputfile="Titanic data profiling.html")
интерактивность в графики Pandas
import pandas as pd
import cufflinks as cf
import plotly.offline
cf.go_offline()
cf.set_config_file(offline=False, world_readable=True)

df.iplot()
