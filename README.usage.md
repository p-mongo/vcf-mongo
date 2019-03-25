Ensure you have jruby installed:

    ruby -v
    # => jruby 9.2.5.0 (2.5.0) 2018-12-06 6d5a228 OpenJDK 64-Bit Server VM 25.171-b11 on 1.8.0_171-8u171-b11-2-b11 +jit [linux-x86_64]

Clone the repository:

    git clone https://github.com/p-mongo/vcf-mongo
    cd vcf-mongo

Build the gem:

    gem build *.gemspec

Install the gem:

    gem install *.gem

Execute the import command:

    vcf-import myCollection file1.vcf file2.vcf.gz ...

Dev import:

    be ruby -I. -Ilib bin/vcf-admin fix test; be ruby -I. -Ilib bin/vcf-import test VCF_40.vcf
