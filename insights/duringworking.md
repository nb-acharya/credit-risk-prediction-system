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

member_id : why member_id? maybe this is just the members of the bank

loan_amnt : amount of money applied as loan from the borrower

funded_amnt : The total amount committed to that loan at that point in time.

funded_amnt_inv: the total amount committed by investors for that loan at that point in time.

term: the number of payments on the loan. Values are in months and can be either 36 or 60.

int_rate: Interest Rate on the loan

installment: The monthly payment owed by the borrower if the loan originates.

grade: LC assigned loan grade

sub_grade: Lc assigned loan subgrade

emp_title: the job title supplied by the borrower when applying for the loan.

emp_length: employment length in years. Possible values are between 0 and 10 where 0 means less than one year and 10 means ten or more years.

home_ownership: The home ownership status provided by the borrower during registration.

annual_inc: the self-reported annual income provided by the borrower during registration

verification_status: 

issue_d: The month which the loan was funded

loan_status: Current status of the loan

pymnt_plan: indicates if a payment plan has been put in place for the loan

url: URL for the LC page with listing data

desc: :Loan description provided by the borrower

purpose: a category provided by the borrower for the loan request.

title: the loan title provided by the borrower

zip_code: The first 3 numbers of the zip code provided by the borrower in the loan application.

addr_state: The state provided by the borrower in the loan application

dti: A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations, excluding mortgage and the requested LC loan, divided by the borrower’s self-reported monthly income.

delinq_2yrs: The number of 30+ days past-due incidences of delinquency in the borrower's credit file for the past 2 years.

earliest_cr_line: The month the borrower's earliest reported credit line was opened

inq_last_6mths: The number of inquiries in past 6 months (excluding auto and mortgage inquiries)

mths_since_last_delinq: The number of months since the borrower's last delinquency.

mths_since_last_record: The number of months since the last public record.

open_acc: The number of open credit lines in the borrower's credit file.

pub_rec: Number of derogatory public records

revol_bal: Total credit revolving balance

revol_util: Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit.

total_acc: The total number of credit lines currently in the borrower's credit file

initial_list_status: The initial listing status of the loan. Possible values are – W, F

out_prncp: Remaining outstanding principal for total amount funded
 
out_prncp_inv: Remaining outstanding principal for portion of total amount funded by investors

total_pymnt: Payments received to date for total amount funded

total_pymnt_inv: Payments received to date for portion of total amount funded by investors

total_rec_prncp: Principal received to date

total_rec_int: Interest received to date

total_rec_late_fee: Late fees received to date

recoveries: post charge off gross recovery

collection_recovery_fee: post charge off collection fee

last_pymnt_d: Last month payment was received

last_pymnt_amnt: Last total payment amount received

next_pymnt_d: Next scheduled payment date

last_credit_pull_d: The most recent month LC pulled credit for this loan

collections_12_mths_ex_med: Number of collections in 12 months excluding medical collections

mths_since_last_major_derog: Months since most recent 90-day or worse rating

policy_code: "publicly available policy_code=1
                new products not publicly available policy_code=2"

application_type: Indicates whether the loan is an individual application or a joint application with two co-borrowers

annual_inc_joint: The combined self-reported annual income provided by the co-borrowers during registration

dti_joint: A ratio calculated using the co-borrowers' total monthly payments on the total debt obligations, excluding mortgages and the requested LC loan, divided by the co-borrowers' combined self-reported monthly income

verification_status_joint:

acc_now_delinq: The number of accounts on which the borrower is now delinquent.

tot_coll_amt: Total collection amounts ever owed

tot_cur_bal: Total current balance of all accounts

open_acc_6m: Number of open trades in last 6 months

open_il_6m: Number of currently active installment trades

open_il_12m: Number of installment accounts opened in past 12 months

open_il_24m: Number of installment accounts opened in past 24 months

mths_since_rcnt_il: Months since most recent installment accounts opened

total_bal_il: Total current balance of all installment accounts

il_util: Ratio of total current balance to high credit/credit limit on all install acct

open_rv_12m: Number of revolving trades opened in past 12 months

open_rv_24m: Number of revolving trades opened in past 24 months

max_bal_bc: Maximum current balance owed on all revolving accounts

all_util: Balance to credit limit on all trades

total_rev_hi_lim: Total revolving high credit/credit limit

inq_fi: Number of personal finance inquiries

total_cu_tl: Number of finance trades

inq_last_12m: Number of credit inquiries in past 12 months


