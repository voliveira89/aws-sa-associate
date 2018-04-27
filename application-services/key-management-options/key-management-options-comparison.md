# Key Management Options Comparison



![](https://lh5.googleusercontent.com/qTyTRe9n2nzqwKtR07K4KWOGZyxGyBpLYSjj115dbgOKbmn82HSmzEN5Qp1f07ABAztM_4jKmz0XyhoB95jHzzO67BBj_eJLFpt76DqQ9wkyyLUJAyNUk8es9nEa-h-5p800US3k)

You should consider using AWS CloudHSM over AWS KMS if you require:

* Keys stored in dedicated, third-party validated hardware security modules under your exclusive control.
* FIPS 140-2 compliance.
* Integration with applications using PKCS\#11, Java JCE, or Microsoft CNG interfaces.
* High-performance in-VPC cryptographic acceleration \(bulk crypto\).

