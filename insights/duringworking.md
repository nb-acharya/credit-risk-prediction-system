C:\Users\niroj\AppData\Local\Temp\ipykernel_24804\59657617.py:1: DtypeWarning: Columns (0: desc, 1: verification_status_joint) have mixed types. Specify dtype option on import or set low_memory=False.
  df = pd.read_csv("../dataset/loan/loan.csv")


-> some kind of warning only, but we can resolve it, we need to look deep into it later, regarding the memory management and data types in pandas



Thought process in the beginning of the project:

This has something to do with loan, right ? 

So what is bank(i dont know if it is a bank, but i guess it is) really interested in? Giving out loans to people, but what does bank get out of it? Well, the idea i have is bank gives out loan to people in certain interest, so the bank get the money back with interest. I think this is the only way banks actaully make money, but again I have very poor knowledge about these economy things, which of course changes today.

So if i have to ask few questions what would they be after looking at the columns myself,and my knowledge in this earth till now:
1. I guess your first question makes sense, that which characteristics of borrower results in default most of the time? we have to identify such characteristics so that bank can predict following characteristics of person is not good for us

I cant think of any more questions, but i feel there is like one main question and rest of questions are just sub branch of that questions, cause in the core we are interested in profit right?

Real goal about this project: expected interest income vs expected default loss.


### Understanding each column

id : maybe just an id
member_id
loan_amnt
funded_amnt
funded_amnt_inv
term
int_rate
installment
grade
sub_grade
emp_title
emp_length
home_ownership
annual_inc
verification_status
issue_d
loan_status
pymnt_plan
url
desc
purpose
title
zip_code
addr_state
dti
delinq_2yrs
earliest_cr_line
inq_last_6mths
mths_since_last_delinq
mths_since_last_record
open_acc
pub_rec
revol_bal
revol_util
total_acc
initial_list_status
out_prncp
out_prncp_inv
total_pymnt
total_pymnt_inv
total_rec_prncp
total_rec_int
total_rec_late_fee
recoveries
collection_recovery_fee
last_pymnt_d
last_pymnt_amnt
next_pymnt_d
last_credit_pull_d
collections_12_mths_ex_med
mths_since_last_major_derog
policy_code
application_type
annual_inc_joint
dti_joint
verification_status_joint
acc_now_delinq
tot_coll_amt
tot_cur_bal
open_acc_6m
open_il_6m
open_il_12m
open_il_24m
mths_since_rcnt_il
total_bal_il
il_util
open_rv_12m
open_rv_24m
max_bal_bc
all_util
total_rev_hi_lim
inq_fi
total_cu_tl
inq_last_12m

