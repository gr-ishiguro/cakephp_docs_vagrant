CakePHP Cookbook(cakephp/docs)���r���h���邽�߂�Vagrant
=======================================================

sphinx�t�H�[�}�b�g�ŏ����ꂽ CakePHP Cookbook(cakephp/docs) �̃t�@�C�����r���h��������ȒP�ɂ��邽�߂̂��̂ł��B
Make�APython�ASphinx �Ȃǂ͂��͂�C���X�g�[������K�v������܂���I
���̑���� Virtual Box �� Vagrant ���g���̂ł��B

�C���X�g�[��
------------

    $ git clone https://github.com/waterada/cakephp_docs_vagrant.git
    $ cd cakephp_docs_vagrant
    $ git submodule update --init

���̌�A`forked_docs_path.conf` ���J���Ă��������B

    $ vi forked_docs_path.conf

�J������A���L�̂悤�ɁAhttps://github.com/cakephp/docs ����t�H�[�N���ăN���[������������ docs �f�B���N�g���̃p�X�ɏ��������܂��B

    /Users/waterada/cakephp/docs

��������

    C:/cakephp/docs

�������āA`vagrant up` ���Ă��������B

    $ vagrant up

�ȏ�ł��B


�r���h
------

���{��̖|����r���h�������Ȃ�:

    $ vagrant ssh
    [vagrant]$ cd /forked_docs

�ŁA�}�E���g����Ă��� docs �̃p�X�܂ňړ����āA

    [vagrant]$ make html-ja

�Ƃ��āA���[�J���́Adocs �̃t�H���_�J���Ă��������Bbuild �Ƃ����t�H���_���o���オ���Ă���͂��ł��B
���̒��Ƀr���h�ς݂̃t�@�C������������Ă��܂��̂ŁA�u���E�U�Œ��ڊJ���Ċm�F���Ă��������B

�ȏ�ł��B



Vagrant to build the cakephp/docs -- CakePHP Cookbook.
======================================================

This is for easy making the envrinment to build sphinx format files of cakephp/docs -- CakePHP Cookbook. It means the Make, Python, Sphinx and so on no longer need to be installed into your PC! Instead, you will use the Virtual Box and Vagrant.

Installing
----------

    $ git clone https://github.com/waterada/cakephp_docs_vagrant.git
    $ cd cakephp_docs_vagrant
    $ git submodule update --init

Then, you need to open `forked_docs_path.conf`:

    $ vi forked_docs_path.conf

And you need to change the path to your cloned docs directory forked from https://github.com/cakephp/docs. For example:

    /Users/waterada/cakephp/docs

or

    C:/cakephp/docs

Then, `vagrant up`.

    $ vagrant up

That's all.


Building
--------

If you'd like to build the Japanese translation, then, after move the mounted `docs` directory:

    $ vagrant ssh
    [vagrant]$ cd /forked_docs

Then, run `make`.

    [vagrant]$ make html-ja

Then, open your local `docs` directory. You will find `build` directory there. You can directly open build files with any browser to check them.

That's all.
