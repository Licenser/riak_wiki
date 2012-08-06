When installing Riak on CentOS or Redhat you can install from source or from our custom .rpm package.

## Notes
  * CentOS enables SE Linux by default and you may need to disable SE Linux if you encounter errors.
  * Erlang OTP R14B03 and Riak Enterprise 1.0.2 do not work on CentOS 5.2, but do work on CentOS 5.3 and newer.

## Installing From Our Custom .rpm Package
### For Centos 5 / RHEL 5
```bash
wget http://downloads.basho.com/riak/CURRENT/riak-1.2.0-1.el5.x86_64.rpm
sudo rpm -Uvh riak-1.2.0-1.el5.x86_64.rpm
```

### For Centos 6 / RHEL 6
```bash
wget http://downloads.basho.com/riak/CURRENT/riak-1.2.0-1.el6.x86_64.rpm
sudo rpm -Uvh riak-1.2.0-1.el6.x86_64.rpm
```

## Installing From Source
Riak requires [[Erlang|http://www.erlang.org/]] R14B03 or later. If you do not have Erlang already installed, see our guide to [[Installing Erlang]]. Don’t worry, it’s easy!

Building from source will require the following packages:

  * gcc
  * gcc-c++
  * glibc-devel
  * make

You can install these with yum:

```basho
sudo yum install gcc gcc-c++ glibc-devel make git

Now we can download and install Riak:

```basho
wget http://downloads.basho.com/riak/CURRENT/riak-1.2.0.tar.gz
tar zxvf riak-1.2.0.tar.gz
cd riak-1.2.0
make rel
```

You will now have a fresh build of Riak in the `rel/riak` directory.

## Next Steps?
From here you might want to check out:

  * [[The Riak Fast Track]]: a guide for setting up a 3 node cluster and exploring Riak’s main features.
  * [[Basic Cluster Setup]]: a guide that will show you how to go from one node to bigger than Google!
