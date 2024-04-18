# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# McFadden’s Choice Model (Alternative-Specific Conditional Logit) Use Package mlogit With (In) R Software
# Conditional logit (McFadden's) choice model Use Package mlogit With (In) R Software
# Install McFadden’s Choice Model (Alternative-Specific Conditional Logit) Use Package mlogit With (In) R Software
# Install Conditional logit (McFadden's) choice model Use Package mlogit With (In) R Software
install.packages("readxl")
install.packages("httr")
install.packages("mlogit")
library("httr")
library("readxl")
library("mlogit")
# Import Data Excel Into R From Github Olah Data Semarang (timbulwidodostp)
github_link <- "https://github.com/timbulwidodostp/mlogit/raw/main/mlogit/mlogit.xlsx"
temp_file <- tempfile(fileext = ".xlsx")
req <- GET(github_link, 
# authenticate using GITHUB_PAT
authenticate(Sys.getenv("GITHUB_PAT"), ""),
# write result to disk
write_disk(path = temp_file))
mlogit <- readxl::read_excel(temp_file)
# Estimate McFadden’s Choice Model (Alternative-Specific Conditional Logit) Use Package mlogit With (In) R Software
model <- mlogit(purchase ~ dealers| gender, data = mlogit)
summary(model)
# McFadden’s Choice Model (Alternative-Specific Conditional Logit) Use Package mlogit With (In) R Software
# Conditional logit (McFadden's) choice model Use Package mlogit With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished