df = pd.merge(df, temp_df, on="<DATE>", how="outer")
	склеивает df и temp_df по столбцу <DATE>,  how говорит оставить те, несовпадающие столбцы