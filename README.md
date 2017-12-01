#edtda2 has a variable named Ratio that varies across different individual groups over time represented by ID.  
#To aggregate ratio across the individual groups over time, say from daily to monthly.
#########averaging the ratio across different months##########
edtda2$Month_Yr <- format(as.Date(edtda2$Year), "%Y-%m")
f=aggregate( Ratio ~ Month_Yr + ID , edtda2 , mean )
