<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:5`](#percona5)
-	[`percona:5.6`](#percona56)
-	[`percona:5.6.45`](#percona5645)
-	[`percona:5.6.45-centos`](#percona5645-centos)
-	[`percona:5.6-centos`](#percona56-centos)
-	[`percona:5.7`](#percona57)
-	[`percona:5.7.26`](#percona5726)
-	[`percona:5.7.26-centos`](#percona5726-centos)
-	[`percona:5.7-centos`](#percona57-centos)
-	[`percona:5-centos`](#percona5-centos)
-	[`percona:8`](#percona8)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0.16-7`](#percona8016-7)
-	[`percona:8.0.16-7-centos`](#percona8016-7-centos)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:centos`](#perconacentos)
-	[`percona:latest`](#perconalatest)
-	[`percona:ps-5`](#perconaps-5)
-	[`percona:ps-5.6`](#perconaps-56)
-	[`percona:ps-5.6.45`](#perconaps-5645)
-	[`percona:ps-5.7`](#perconaps-57)
-	[`percona:ps-5.7.26`](#perconaps-5726)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.16-7`](#perconaps-8016-7)
-	[`percona:psmdb-3.6`](#perconapsmdb-36)
-	[`percona:psmdb-3.6.16`](#perconapsmdb-3616)
-	[`percona:psmdb-4.0`](#perconapsmdb-40)
-	[`percona:psmdb-4.0.14`](#perconapsmdb-4014)

## `percona:5`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:5` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.6`

```console
$ docker pull percona@sha256:5c375584ae28ca15e9fbbbf9932cc6af91b7082d35aaced59ae49123aaa66136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:5.6` - linux; amd64

```console
$ docker pull percona@sha256:37d72d3974c370f591f9e9047c3942a9545d585db7cc43e52b1be9656426a87f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138883132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b62677e11375e3b986227904ea911bf63eca0d8e43edb6a70ecac8e09f7530`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 20 Aug 2019 20:21:00 GMT
ADD file:4e7247c06de9ad117293b6bf39c77f96c623a1bca4da35068d7e64c7cb826c08 in / 
# Tue, 20 Aug 2019 20:21:01 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20190801
# Tue, 20 Aug 2019 20:21:01 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2019 20:29:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 20 Aug 2019 20:30:35 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 20 Aug 2019 20:30:36 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 20 Aug 2019 20:31:41 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/centos/7/RPMS/noarch/percona-release-0.1-8.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release enable percona release
# Tue, 20 Aug 2019 20:31:42 GMT
ENV PERCONA_VERSION=5.6.45-rel86.1.el7
# Tue, 20 Aug 2019 20:32:18 GMT
RUN yum install -y 		Percona-Server-server-56-${PERCONA_VERSION} 		Percona-Server-tokudb-56-${PERCONA_VERSION} 		Percona-Server-rocksdb-56-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 20 Aug 2019 20:32:19 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 20 Aug 2019 20:32:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 20 Aug 2019 20:32:19 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Tue, 20 Aug 2019 20:32:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Aug 2019 20:32:20 GMT
USER mysql
# Tue, 20 Aug 2019 20:32:20 GMT
EXPOSE 3306
# Tue, 20 Aug 2019 20:32:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d8d02d45731499028db01b6fa35475f91d230628b4e25fab8e3c015594dc3261`  
		Last Modified: Tue, 20 Aug 2019 20:23:41 GMT  
		Size: 75.4 MB (75412258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f77467aecaf2b9d4d65a97662a3f889d6ceb9d6672047c27ab7944320a29bc`  
		Last Modified: Tue, 20 Aug 2019 20:35:38 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c07efe7d4350efd17328a8bd1d5981bb8d2e2e6d8fe2f9c8ad71c5ae547397`  
		Last Modified: Tue, 20 Aug 2019 20:35:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da175e2c11837a692a1a2d160bdd1f33e4fe642a8a3fc3d5f5388ab782a0a32`  
		Last Modified: Tue, 20 Aug 2019 20:36:08 GMT  
		Size: 6.2 MB (6169820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206841e3e34cb887c17be880b17a2d899379c7b3ee3a3dc244977fa9fb843901`  
		Last Modified: Tue, 20 Aug 2019 20:36:17 GMT  
		Size: 57.3 MB (57291271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7602f0ae8f46f29fd3df7f540fb2883638098b63e4b678db6c00376d494df05`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 4.9 KB (4882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524799dae228b7ad0b99191702914068221c075596aaffeb6a9447348b60d88e`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.6.45`

```console
$ docker pull percona@sha256:5c375584ae28ca15e9fbbbf9932cc6af91b7082d35aaced59ae49123aaa66136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:5.6.45` - linux; amd64

```console
$ docker pull percona@sha256:37d72d3974c370f591f9e9047c3942a9545d585db7cc43e52b1be9656426a87f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138883132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b62677e11375e3b986227904ea911bf63eca0d8e43edb6a70ecac8e09f7530`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 20 Aug 2019 20:21:00 GMT
ADD file:4e7247c06de9ad117293b6bf39c77f96c623a1bca4da35068d7e64c7cb826c08 in / 
# Tue, 20 Aug 2019 20:21:01 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20190801
# Tue, 20 Aug 2019 20:21:01 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2019 20:29:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 20 Aug 2019 20:30:35 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 20 Aug 2019 20:30:36 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 20 Aug 2019 20:31:41 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/centos/7/RPMS/noarch/percona-release-0.1-8.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release enable percona release
# Tue, 20 Aug 2019 20:31:42 GMT
ENV PERCONA_VERSION=5.6.45-rel86.1.el7
# Tue, 20 Aug 2019 20:32:18 GMT
RUN yum install -y 		Percona-Server-server-56-${PERCONA_VERSION} 		Percona-Server-tokudb-56-${PERCONA_VERSION} 		Percona-Server-rocksdb-56-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 20 Aug 2019 20:32:19 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 20 Aug 2019 20:32:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 20 Aug 2019 20:32:19 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Tue, 20 Aug 2019 20:32:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Aug 2019 20:32:20 GMT
USER mysql
# Tue, 20 Aug 2019 20:32:20 GMT
EXPOSE 3306
# Tue, 20 Aug 2019 20:32:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d8d02d45731499028db01b6fa35475f91d230628b4e25fab8e3c015594dc3261`  
		Last Modified: Tue, 20 Aug 2019 20:23:41 GMT  
		Size: 75.4 MB (75412258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f77467aecaf2b9d4d65a97662a3f889d6ceb9d6672047c27ab7944320a29bc`  
		Last Modified: Tue, 20 Aug 2019 20:35:38 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c07efe7d4350efd17328a8bd1d5981bb8d2e2e6d8fe2f9c8ad71c5ae547397`  
		Last Modified: Tue, 20 Aug 2019 20:35:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da175e2c11837a692a1a2d160bdd1f33e4fe642a8a3fc3d5f5388ab782a0a32`  
		Last Modified: Tue, 20 Aug 2019 20:36:08 GMT  
		Size: 6.2 MB (6169820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206841e3e34cb887c17be880b17a2d899379c7b3ee3a3dc244977fa9fb843901`  
		Last Modified: Tue, 20 Aug 2019 20:36:17 GMT  
		Size: 57.3 MB (57291271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7602f0ae8f46f29fd3df7f540fb2883638098b63e4b678db6c00376d494df05`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 4.9 KB (4882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524799dae228b7ad0b99191702914068221c075596aaffeb6a9447348b60d88e`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.6.45-centos`

```console
$ docker pull percona@sha256:5c375584ae28ca15e9fbbbf9932cc6af91b7082d35aaced59ae49123aaa66136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:5.6.45-centos` - linux; amd64

```console
$ docker pull percona@sha256:37d72d3974c370f591f9e9047c3942a9545d585db7cc43e52b1be9656426a87f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138883132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b62677e11375e3b986227904ea911bf63eca0d8e43edb6a70ecac8e09f7530`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 20 Aug 2019 20:21:00 GMT
ADD file:4e7247c06de9ad117293b6bf39c77f96c623a1bca4da35068d7e64c7cb826c08 in / 
# Tue, 20 Aug 2019 20:21:01 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20190801
# Tue, 20 Aug 2019 20:21:01 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2019 20:29:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 20 Aug 2019 20:30:35 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 20 Aug 2019 20:30:36 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 20 Aug 2019 20:31:41 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/centos/7/RPMS/noarch/percona-release-0.1-8.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release enable percona release
# Tue, 20 Aug 2019 20:31:42 GMT
ENV PERCONA_VERSION=5.6.45-rel86.1.el7
# Tue, 20 Aug 2019 20:32:18 GMT
RUN yum install -y 		Percona-Server-server-56-${PERCONA_VERSION} 		Percona-Server-tokudb-56-${PERCONA_VERSION} 		Percona-Server-rocksdb-56-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 20 Aug 2019 20:32:19 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 20 Aug 2019 20:32:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 20 Aug 2019 20:32:19 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Tue, 20 Aug 2019 20:32:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Aug 2019 20:32:20 GMT
USER mysql
# Tue, 20 Aug 2019 20:32:20 GMT
EXPOSE 3306
# Tue, 20 Aug 2019 20:32:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d8d02d45731499028db01b6fa35475f91d230628b4e25fab8e3c015594dc3261`  
		Last Modified: Tue, 20 Aug 2019 20:23:41 GMT  
		Size: 75.4 MB (75412258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f77467aecaf2b9d4d65a97662a3f889d6ceb9d6672047c27ab7944320a29bc`  
		Last Modified: Tue, 20 Aug 2019 20:35:38 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c07efe7d4350efd17328a8bd1d5981bb8d2e2e6d8fe2f9c8ad71c5ae547397`  
		Last Modified: Tue, 20 Aug 2019 20:35:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da175e2c11837a692a1a2d160bdd1f33e4fe642a8a3fc3d5f5388ab782a0a32`  
		Last Modified: Tue, 20 Aug 2019 20:36:08 GMT  
		Size: 6.2 MB (6169820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206841e3e34cb887c17be880b17a2d899379c7b3ee3a3dc244977fa9fb843901`  
		Last Modified: Tue, 20 Aug 2019 20:36:17 GMT  
		Size: 57.3 MB (57291271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7602f0ae8f46f29fd3df7f540fb2883638098b63e4b678db6c00376d494df05`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 4.9 KB (4882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524799dae228b7ad0b99191702914068221c075596aaffeb6a9447348b60d88e`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.6-centos`

```console
$ docker pull percona@sha256:5c375584ae28ca15e9fbbbf9932cc6af91b7082d35aaced59ae49123aaa66136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:5.6-centos` - linux; amd64

```console
$ docker pull percona@sha256:37d72d3974c370f591f9e9047c3942a9545d585db7cc43e52b1be9656426a87f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138883132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b62677e11375e3b986227904ea911bf63eca0d8e43edb6a70ecac8e09f7530`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 20 Aug 2019 20:21:00 GMT
ADD file:4e7247c06de9ad117293b6bf39c77f96c623a1bca4da35068d7e64c7cb826c08 in / 
# Tue, 20 Aug 2019 20:21:01 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20190801
# Tue, 20 Aug 2019 20:21:01 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2019 20:29:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 20 Aug 2019 20:30:35 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 20 Aug 2019 20:30:36 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 20 Aug 2019 20:31:41 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/centos/7/RPMS/noarch/percona-release-0.1-8.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release enable percona release
# Tue, 20 Aug 2019 20:31:42 GMT
ENV PERCONA_VERSION=5.6.45-rel86.1.el7
# Tue, 20 Aug 2019 20:32:18 GMT
RUN yum install -y 		Percona-Server-server-56-${PERCONA_VERSION} 		Percona-Server-tokudb-56-${PERCONA_VERSION} 		Percona-Server-rocksdb-56-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 20 Aug 2019 20:32:19 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 20 Aug 2019 20:32:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 20 Aug 2019 20:32:19 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Tue, 20 Aug 2019 20:32:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Aug 2019 20:32:20 GMT
USER mysql
# Tue, 20 Aug 2019 20:32:20 GMT
EXPOSE 3306
# Tue, 20 Aug 2019 20:32:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d8d02d45731499028db01b6fa35475f91d230628b4e25fab8e3c015594dc3261`  
		Last Modified: Tue, 20 Aug 2019 20:23:41 GMT  
		Size: 75.4 MB (75412258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f77467aecaf2b9d4d65a97662a3f889d6ceb9d6672047c27ab7944320a29bc`  
		Last Modified: Tue, 20 Aug 2019 20:35:38 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c07efe7d4350efd17328a8bd1d5981bb8d2e2e6d8fe2f9c8ad71c5ae547397`  
		Last Modified: Tue, 20 Aug 2019 20:35:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da175e2c11837a692a1a2d160bdd1f33e4fe642a8a3fc3d5f5388ab782a0a32`  
		Last Modified: Tue, 20 Aug 2019 20:36:08 GMT  
		Size: 6.2 MB (6169820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206841e3e34cb887c17be880b17a2d899379c7b3ee3a3dc244977fa9fb843901`  
		Last Modified: Tue, 20 Aug 2019 20:36:17 GMT  
		Size: 57.3 MB (57291271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7602f0ae8f46f29fd3df7f540fb2883638098b63e4b678db6c00376d494df05`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 4.9 KB (4882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524799dae228b7ad0b99191702914068221c075596aaffeb6a9447348b60d88e`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:5.7` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.26`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:5.7.26` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7.26-centos`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:5.7.26-centos` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5.7-centos`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:5.7-centos` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:5-centos`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:5-centos` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8`

```console
$ docker pull percona@sha256:72f7e06c3929d6d2636a0f4d6d02bb117c8b3b0991491236a99b09783fca344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:e442b0d658ae944c0144c04bb3e676b7bc1d0f6b76d4681a82522f2b6e9e9200
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212495235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170ff500920bc13e16ff63ea47d0b338e8a7f3fe4bc37ec40ad24666c908bded`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:17:32 GMT
RUN groupadd -g 1001 mysql
# Tue, 12 Nov 2019 02:17:33 GMT
RUN useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:17:40 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release setup ps80
# Tue, 12 Nov 2019 02:17:40 GMT
ENV PERCONA_VERSION=8.0.16-7.1.el7
# Tue, 12 Nov 2019 02:18:45 GMT
RUN yum install -y 		percona-server-server-${PERCONA_VERSION} 		percona-server-tokudb-${PERCONA_VERSION} 		percona-server-rocksdb-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:18:46 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 12 Nov 2019 02:18:46 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:18:47 GMT
COPY file:98315a3cdd5c008868bca89eff8d9037073d3b25d79ce0bfce9220868c87243b in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:18:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:18:47 GMT
USER mysql
# Tue, 12 Nov 2019 02:18:47 GMT
EXPOSE 3306 33060
# Tue, 12 Nov 2019 02:18:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd87aed0b083cb1b639d2dd7663d85166a65b7f00423492d3fc893b46ba1efa1`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41c0be21edf06063e243b167324669066e08e5d4bd8b67f13875d6b3690c346`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc216c52e445aae86a60a1dd1d290b2bb31c001c827f7c8296fd28386dde5828`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 6.4 MB (6437188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851dfa885f2912de0bead50f3f1788ee494476faa2edb3439c7339bd5c921ba`  
		Last Modified: Tue, 12 Nov 2019 02:23:32 GMT  
		Size: 130.3 MB (130271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788672c6ab1554ba42ba03b003c232b97c4c9b4eceb9bf21b0f856f4536cf88`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd546236c6797e65a5d97a0c13fbdcad96d4eab143d0fbc1400d80b9cd85cf8`  
		Last Modified: Tue, 12 Nov 2019 02:23:06 GMT  
		Size: 3.1 KB (3068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0`

```console
$ docker pull percona@sha256:72f7e06c3929d6d2636a0f4d6d02bb117c8b3b0991491236a99b09783fca344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:e442b0d658ae944c0144c04bb3e676b7bc1d0f6b76d4681a82522f2b6e9e9200
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212495235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170ff500920bc13e16ff63ea47d0b338e8a7f3fe4bc37ec40ad24666c908bded`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:17:32 GMT
RUN groupadd -g 1001 mysql
# Tue, 12 Nov 2019 02:17:33 GMT
RUN useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:17:40 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release setup ps80
# Tue, 12 Nov 2019 02:17:40 GMT
ENV PERCONA_VERSION=8.0.16-7.1.el7
# Tue, 12 Nov 2019 02:18:45 GMT
RUN yum install -y 		percona-server-server-${PERCONA_VERSION} 		percona-server-tokudb-${PERCONA_VERSION} 		percona-server-rocksdb-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:18:46 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 12 Nov 2019 02:18:46 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:18:47 GMT
COPY file:98315a3cdd5c008868bca89eff8d9037073d3b25d79ce0bfce9220868c87243b in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:18:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:18:47 GMT
USER mysql
# Tue, 12 Nov 2019 02:18:47 GMT
EXPOSE 3306 33060
# Tue, 12 Nov 2019 02:18:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd87aed0b083cb1b639d2dd7663d85166a65b7f00423492d3fc893b46ba1efa1`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41c0be21edf06063e243b167324669066e08e5d4bd8b67f13875d6b3690c346`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc216c52e445aae86a60a1dd1d290b2bb31c001c827f7c8296fd28386dde5828`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 6.4 MB (6437188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851dfa885f2912de0bead50f3f1788ee494476faa2edb3439c7339bd5c921ba`  
		Last Modified: Tue, 12 Nov 2019 02:23:32 GMT  
		Size: 130.3 MB (130271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788672c6ab1554ba42ba03b003c232b97c4c9b4eceb9bf21b0f856f4536cf88`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd546236c6797e65a5d97a0c13fbdcad96d4eab143d0fbc1400d80b9cd85cf8`  
		Last Modified: Tue, 12 Nov 2019 02:23:06 GMT  
		Size: 3.1 KB (3068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.16-7`

```console
$ docker pull percona@sha256:72f7e06c3929d6d2636a0f4d6d02bb117c8b3b0991491236a99b09783fca344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:8.0.16-7` - linux; amd64

```console
$ docker pull percona@sha256:e442b0d658ae944c0144c04bb3e676b7bc1d0f6b76d4681a82522f2b6e9e9200
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212495235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170ff500920bc13e16ff63ea47d0b338e8a7f3fe4bc37ec40ad24666c908bded`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:17:32 GMT
RUN groupadd -g 1001 mysql
# Tue, 12 Nov 2019 02:17:33 GMT
RUN useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:17:40 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release setup ps80
# Tue, 12 Nov 2019 02:17:40 GMT
ENV PERCONA_VERSION=8.0.16-7.1.el7
# Tue, 12 Nov 2019 02:18:45 GMT
RUN yum install -y 		percona-server-server-${PERCONA_VERSION} 		percona-server-tokudb-${PERCONA_VERSION} 		percona-server-rocksdb-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:18:46 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 12 Nov 2019 02:18:46 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:18:47 GMT
COPY file:98315a3cdd5c008868bca89eff8d9037073d3b25d79ce0bfce9220868c87243b in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:18:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:18:47 GMT
USER mysql
# Tue, 12 Nov 2019 02:18:47 GMT
EXPOSE 3306 33060
# Tue, 12 Nov 2019 02:18:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd87aed0b083cb1b639d2dd7663d85166a65b7f00423492d3fc893b46ba1efa1`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41c0be21edf06063e243b167324669066e08e5d4bd8b67f13875d6b3690c346`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc216c52e445aae86a60a1dd1d290b2bb31c001c827f7c8296fd28386dde5828`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 6.4 MB (6437188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851dfa885f2912de0bead50f3f1788ee494476faa2edb3439c7339bd5c921ba`  
		Last Modified: Tue, 12 Nov 2019 02:23:32 GMT  
		Size: 130.3 MB (130271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788672c6ab1554ba42ba03b003c232b97c4c9b4eceb9bf21b0f856f4536cf88`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd546236c6797e65a5d97a0c13fbdcad96d4eab143d0fbc1400d80b9cd85cf8`  
		Last Modified: Tue, 12 Nov 2019 02:23:06 GMT  
		Size: 3.1 KB (3068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0.16-7-centos`

```console
$ docker pull percona@sha256:72f7e06c3929d6d2636a0f4d6d02bb117c8b3b0991491236a99b09783fca344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:8.0.16-7-centos` - linux; amd64

```console
$ docker pull percona@sha256:e442b0d658ae944c0144c04bb3e676b7bc1d0f6b76d4681a82522f2b6e9e9200
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212495235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170ff500920bc13e16ff63ea47d0b338e8a7f3fe4bc37ec40ad24666c908bded`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:17:32 GMT
RUN groupadd -g 1001 mysql
# Tue, 12 Nov 2019 02:17:33 GMT
RUN useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:17:40 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release setup ps80
# Tue, 12 Nov 2019 02:17:40 GMT
ENV PERCONA_VERSION=8.0.16-7.1.el7
# Tue, 12 Nov 2019 02:18:45 GMT
RUN yum install -y 		percona-server-server-${PERCONA_VERSION} 		percona-server-tokudb-${PERCONA_VERSION} 		percona-server-rocksdb-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:18:46 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 12 Nov 2019 02:18:46 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:18:47 GMT
COPY file:98315a3cdd5c008868bca89eff8d9037073d3b25d79ce0bfce9220868c87243b in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:18:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:18:47 GMT
USER mysql
# Tue, 12 Nov 2019 02:18:47 GMT
EXPOSE 3306 33060
# Tue, 12 Nov 2019 02:18:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd87aed0b083cb1b639d2dd7663d85166a65b7f00423492d3fc893b46ba1efa1`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41c0be21edf06063e243b167324669066e08e5d4bd8b67f13875d6b3690c346`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc216c52e445aae86a60a1dd1d290b2bb31c001c827f7c8296fd28386dde5828`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 6.4 MB (6437188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851dfa885f2912de0bead50f3f1788ee494476faa2edb3439c7339bd5c921ba`  
		Last Modified: Tue, 12 Nov 2019 02:23:32 GMT  
		Size: 130.3 MB (130271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788672c6ab1554ba42ba03b003c232b97c4c9b4eceb9bf21b0f856f4536cf88`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd546236c6797e65a5d97a0c13fbdcad96d4eab143d0fbc1400d80b9cd85cf8`  
		Last Modified: Tue, 12 Nov 2019 02:23:06 GMT  
		Size: 3.1 KB (3068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:72f7e06c3929d6d2636a0f4d6d02bb117c8b3b0991491236a99b09783fca344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:e442b0d658ae944c0144c04bb3e676b7bc1d0f6b76d4681a82522f2b6e9e9200
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212495235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170ff500920bc13e16ff63ea47d0b338e8a7f3fe4bc37ec40ad24666c908bded`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:17:32 GMT
RUN groupadd -g 1001 mysql
# Tue, 12 Nov 2019 02:17:33 GMT
RUN useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:17:40 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release setup ps80
# Tue, 12 Nov 2019 02:17:40 GMT
ENV PERCONA_VERSION=8.0.16-7.1.el7
# Tue, 12 Nov 2019 02:18:45 GMT
RUN yum install -y 		percona-server-server-${PERCONA_VERSION} 		percona-server-tokudb-${PERCONA_VERSION} 		percona-server-rocksdb-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:18:46 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 12 Nov 2019 02:18:46 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:18:47 GMT
COPY file:98315a3cdd5c008868bca89eff8d9037073d3b25d79ce0bfce9220868c87243b in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:18:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:18:47 GMT
USER mysql
# Tue, 12 Nov 2019 02:18:47 GMT
EXPOSE 3306 33060
# Tue, 12 Nov 2019 02:18:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd87aed0b083cb1b639d2dd7663d85166a65b7f00423492d3fc893b46ba1efa1`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41c0be21edf06063e243b167324669066e08e5d4bd8b67f13875d6b3690c346`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc216c52e445aae86a60a1dd1d290b2bb31c001c827f7c8296fd28386dde5828`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 6.4 MB (6437188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851dfa885f2912de0bead50f3f1788ee494476faa2edb3439c7339bd5c921ba`  
		Last Modified: Tue, 12 Nov 2019 02:23:32 GMT  
		Size: 130.3 MB (130271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788672c6ab1554ba42ba03b003c232b97c4c9b4eceb9bf21b0f856f4536cf88`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd546236c6797e65a5d97a0c13fbdcad96d4eab143d0fbc1400d80b9cd85cf8`  
		Last Modified: Tue, 12 Nov 2019 02:23:06 GMT  
		Size: 3.1 KB (3068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:8-centos`

```console
$ docker pull percona@sha256:72f7e06c3929d6d2636a0f4d6d02bb117c8b3b0991491236a99b09783fca344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:e442b0d658ae944c0144c04bb3e676b7bc1d0f6b76d4681a82522f2b6e9e9200
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212495235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170ff500920bc13e16ff63ea47d0b338e8a7f3fe4bc37ec40ad24666c908bded`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:17:32 GMT
RUN groupadd -g 1001 mysql
# Tue, 12 Nov 2019 02:17:33 GMT
RUN useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:17:40 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release setup ps80
# Tue, 12 Nov 2019 02:17:40 GMT
ENV PERCONA_VERSION=8.0.16-7.1.el7
# Tue, 12 Nov 2019 02:18:45 GMT
RUN yum install -y 		percona-server-server-${PERCONA_VERSION} 		percona-server-tokudb-${PERCONA_VERSION} 		percona-server-rocksdb-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:18:46 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 12 Nov 2019 02:18:46 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:18:47 GMT
COPY file:98315a3cdd5c008868bca89eff8d9037073d3b25d79ce0bfce9220868c87243b in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:18:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:18:47 GMT
USER mysql
# Tue, 12 Nov 2019 02:18:47 GMT
EXPOSE 3306 33060
# Tue, 12 Nov 2019 02:18:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd87aed0b083cb1b639d2dd7663d85166a65b7f00423492d3fc893b46ba1efa1`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41c0be21edf06063e243b167324669066e08e5d4bd8b67f13875d6b3690c346`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc216c52e445aae86a60a1dd1d290b2bb31c001c827f7c8296fd28386dde5828`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 6.4 MB (6437188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851dfa885f2912de0bead50f3f1788ee494476faa2edb3439c7339bd5c921ba`  
		Last Modified: Tue, 12 Nov 2019 02:23:32 GMT  
		Size: 130.3 MB (130271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788672c6ab1554ba42ba03b003c232b97c4c9b4eceb9bf21b0f856f4536cf88`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd546236c6797e65a5d97a0c13fbdcad96d4eab143d0fbc1400d80b9cd85cf8`  
		Last Modified: Tue, 12 Nov 2019 02:23:06 GMT  
		Size: 3.1 KB (3068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:centos`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:centos` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:latest`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:latest` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-5` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.6`

```console
$ docker pull percona@sha256:5c375584ae28ca15e9fbbbf9932cc6af91b7082d35aaced59ae49123aaa66136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-5.6` - linux; amd64

```console
$ docker pull percona@sha256:37d72d3974c370f591f9e9047c3942a9545d585db7cc43e52b1be9656426a87f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138883132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b62677e11375e3b986227904ea911bf63eca0d8e43edb6a70ecac8e09f7530`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 20 Aug 2019 20:21:00 GMT
ADD file:4e7247c06de9ad117293b6bf39c77f96c623a1bca4da35068d7e64c7cb826c08 in / 
# Tue, 20 Aug 2019 20:21:01 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20190801
# Tue, 20 Aug 2019 20:21:01 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2019 20:29:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 20 Aug 2019 20:30:35 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 20 Aug 2019 20:30:36 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 20 Aug 2019 20:31:41 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/centos/7/RPMS/noarch/percona-release-0.1-8.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release enable percona release
# Tue, 20 Aug 2019 20:31:42 GMT
ENV PERCONA_VERSION=5.6.45-rel86.1.el7
# Tue, 20 Aug 2019 20:32:18 GMT
RUN yum install -y 		Percona-Server-server-56-${PERCONA_VERSION} 		Percona-Server-tokudb-56-${PERCONA_VERSION} 		Percona-Server-rocksdb-56-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 20 Aug 2019 20:32:19 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 20 Aug 2019 20:32:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 20 Aug 2019 20:32:19 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Tue, 20 Aug 2019 20:32:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Aug 2019 20:32:20 GMT
USER mysql
# Tue, 20 Aug 2019 20:32:20 GMT
EXPOSE 3306
# Tue, 20 Aug 2019 20:32:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d8d02d45731499028db01b6fa35475f91d230628b4e25fab8e3c015594dc3261`  
		Last Modified: Tue, 20 Aug 2019 20:23:41 GMT  
		Size: 75.4 MB (75412258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f77467aecaf2b9d4d65a97662a3f889d6ceb9d6672047c27ab7944320a29bc`  
		Last Modified: Tue, 20 Aug 2019 20:35:38 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c07efe7d4350efd17328a8bd1d5981bb8d2e2e6d8fe2f9c8ad71c5ae547397`  
		Last Modified: Tue, 20 Aug 2019 20:35:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da175e2c11837a692a1a2d160bdd1f33e4fe642a8a3fc3d5f5388ab782a0a32`  
		Last Modified: Tue, 20 Aug 2019 20:36:08 GMT  
		Size: 6.2 MB (6169820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206841e3e34cb887c17be880b17a2d899379c7b3ee3a3dc244977fa9fb843901`  
		Last Modified: Tue, 20 Aug 2019 20:36:17 GMT  
		Size: 57.3 MB (57291271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7602f0ae8f46f29fd3df7f540fb2883638098b63e4b678db6c00376d494df05`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 4.9 KB (4882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524799dae228b7ad0b99191702914068221c075596aaffeb6a9447348b60d88e`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.6.45`

```console
$ docker pull percona@sha256:5c375584ae28ca15e9fbbbf9932cc6af91b7082d35aaced59ae49123aaa66136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-5.6.45` - linux; amd64

```console
$ docker pull percona@sha256:37d72d3974c370f591f9e9047c3942a9545d585db7cc43e52b1be9656426a87f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138883132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b62677e11375e3b986227904ea911bf63eca0d8e43edb6a70ecac8e09f7530`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 20 Aug 2019 20:21:00 GMT
ADD file:4e7247c06de9ad117293b6bf39c77f96c623a1bca4da35068d7e64c7cb826c08 in / 
# Tue, 20 Aug 2019 20:21:01 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20190801
# Tue, 20 Aug 2019 20:21:01 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2019 20:29:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 20 Aug 2019 20:30:35 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 20 Aug 2019 20:30:36 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 20 Aug 2019 20:31:41 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/centos/7/RPMS/noarch/percona-release-0.1-8.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release enable percona release
# Tue, 20 Aug 2019 20:31:42 GMT
ENV PERCONA_VERSION=5.6.45-rel86.1.el7
# Tue, 20 Aug 2019 20:32:18 GMT
RUN yum install -y 		Percona-Server-server-56-${PERCONA_VERSION} 		Percona-Server-tokudb-56-${PERCONA_VERSION} 		Percona-Server-rocksdb-56-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 20 Aug 2019 20:32:19 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /etc/my.cnf.d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user|sql_mode)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user|sql_mode)/#&/' 	&& sed -i '/Make sure only root/,/fi/d' /usr/bin/ps_tokudb_admin 	&& echo "thp-setting=never" >> /etc/my.cnf 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 20 Aug 2019 20:32:19 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 20 Aug 2019 20:32:19 GMT
COPY file:1d7c9d67c6f11e6632845ae6085c57582457d49c5e3d732f0b3bd3f40b8bf179 in /docker-entrypoint.sh 
# Tue, 20 Aug 2019 20:32:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Aug 2019 20:32:20 GMT
USER mysql
# Tue, 20 Aug 2019 20:32:20 GMT
EXPOSE 3306
# Tue, 20 Aug 2019 20:32:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d8d02d45731499028db01b6fa35475f91d230628b4e25fab8e3c015594dc3261`  
		Last Modified: Tue, 20 Aug 2019 20:23:41 GMT  
		Size: 75.4 MB (75412258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f77467aecaf2b9d4d65a97662a3f889d6ceb9d6672047c27ab7944320a29bc`  
		Last Modified: Tue, 20 Aug 2019 20:35:38 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c07efe7d4350efd17328a8bd1d5981bb8d2e2e6d8fe2f9c8ad71c5ae547397`  
		Last Modified: Tue, 20 Aug 2019 20:35:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da175e2c11837a692a1a2d160bdd1f33e4fe642a8a3fc3d5f5388ab782a0a32`  
		Last Modified: Tue, 20 Aug 2019 20:36:08 GMT  
		Size: 6.2 MB (6169820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206841e3e34cb887c17be880b17a2d899379c7b3ee3a3dc244977fa9fb843901`  
		Last Modified: Tue, 20 Aug 2019 20:36:17 GMT  
		Size: 57.3 MB (57291271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7602f0ae8f46f29fd3df7f540fb2883638098b63e4b678db6c00376d494df05`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 4.9 KB (4882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524799dae228b7ad0b99191702914068221c075596aaffeb6a9447348b60d88e`  
		Last Modified: Tue, 20 Aug 2019 20:36:06 GMT  
		Size: 2.9 KB (2942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-5.7` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-5.7.26`

```console
$ docker pull percona@sha256:11aac0d0941b5ee1cfe61da2146be9a743ef01e1afdb07e37e70381feefd35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-5.7.26` - linux; amd64

```console
$ docker pull percona@sha256:4805be33414d8f1dbbd3b7968e480fb188a0e0f269970ea72daa93fc2779ee91
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7138331e55af84f13f4ff4dc5e86cfff60cfd1bd3e0b386c8898ba98bcf395`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:19:00 GMT
RUN groupdel input && groupadd -g 999 mysql
# Tue, 12 Nov 2019 02:19:01 GMT
RUN useradd -u 999 -r -g 999 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:19:04 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-0.1-10.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && percona-release enable original release
# Tue, 12 Nov 2019 02:19:04 GMT
ENV PERCONA_VERSION=5.7.26-29.1.el7
# Tue, 12 Nov 2019 02:19:53 GMT
RUN yum install -y 		Percona-Server-server-57-${PERCONA_VERSION} 		Percona-Server-tokudb-57-${PERCONA_VERSION} 		Percona-Server-rocksdb-57-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:19:54 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& ln -s /etc/my.cnf.d /etc/mysql 	&& chown -R mysql:root /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/percona-server.cnf /etc/percona-server.conf.d /etc/my.cnf.d
# Tue, 12 Nov 2019 02:19:54 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:19:55 GMT
COPY file:c0030f6126b4c593910528e74d1ac06ecb2f830c727833843145dece71866501 in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:19:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:19:55 GMT
USER mysql
# Tue, 12 Nov 2019 02:19:55 GMT
EXPOSE 3306
# Tue, 12 Nov 2019 02:19:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7257b8fcee70cacf379da3a66992cff5fe05b7cc65a347d37e86403202bec14d`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b545f5752d4a1df3eac116502b1bd3a5497c90aeb41f18a205f24826235aa3`  
		Last Modified: Tue, 12 Nov 2019 02:23:42 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb8d62436d5387439ed939cf36e8eb4e8d2f01309c52ec943fc97753295ed7`  
		Last Modified: Tue, 12 Nov 2019 02:23:44 GMT  
		Size: 6.4 MB (6438278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624a39ec4a7595ed4c7f6d2f094d2a87c08ac87a369ae7fdd7c6507480ece5b`  
		Last Modified: Tue, 12 Nov 2019 02:24:02 GMT  
		Size: 111.4 MB (111386961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018d615106c7cb9132ab6a2b60728fdba8c829aa16e4a39c335ff6af74f2a024`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c76fd7db438956974e16f3cfa16acba6274af18ce3bb9db8bccaa4de45309f0`  
		Last Modified: Tue, 12 Nov 2019 02:23:43 GMT  
		Size: 3.1 KB (3065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8`

```console
$ docker pull percona@sha256:72f7e06c3929d6d2636a0f4d6d02bb117c8b3b0991491236a99b09783fca344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:e442b0d658ae944c0144c04bb3e676b7bc1d0f6b76d4681a82522f2b6e9e9200
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212495235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170ff500920bc13e16ff63ea47d0b338e8a7f3fe4bc37ec40ad24666c908bded`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:17:32 GMT
RUN groupadd -g 1001 mysql
# Tue, 12 Nov 2019 02:17:33 GMT
RUN useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:17:40 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release setup ps80
# Tue, 12 Nov 2019 02:17:40 GMT
ENV PERCONA_VERSION=8.0.16-7.1.el7
# Tue, 12 Nov 2019 02:18:45 GMT
RUN yum install -y 		percona-server-server-${PERCONA_VERSION} 		percona-server-tokudb-${PERCONA_VERSION} 		percona-server-rocksdb-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:18:46 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 12 Nov 2019 02:18:46 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:18:47 GMT
COPY file:98315a3cdd5c008868bca89eff8d9037073d3b25d79ce0bfce9220868c87243b in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:18:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:18:47 GMT
USER mysql
# Tue, 12 Nov 2019 02:18:47 GMT
EXPOSE 3306 33060
# Tue, 12 Nov 2019 02:18:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd87aed0b083cb1b639d2dd7663d85166a65b7f00423492d3fc893b46ba1efa1`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41c0be21edf06063e243b167324669066e08e5d4bd8b67f13875d6b3690c346`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc216c52e445aae86a60a1dd1d290b2bb31c001c827f7c8296fd28386dde5828`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 6.4 MB (6437188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851dfa885f2912de0bead50f3f1788ee494476faa2edb3439c7339bd5c921ba`  
		Last Modified: Tue, 12 Nov 2019 02:23:32 GMT  
		Size: 130.3 MB (130271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788672c6ab1554ba42ba03b003c232b97c4c9b4eceb9bf21b0f856f4536cf88`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd546236c6797e65a5d97a0c13fbdcad96d4eab143d0fbc1400d80b9cd85cf8`  
		Last Modified: Tue, 12 Nov 2019 02:23:06 GMT  
		Size: 3.1 KB (3068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:72f7e06c3929d6d2636a0f4d6d02bb117c8b3b0991491236a99b09783fca344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:e442b0d658ae944c0144c04bb3e676b7bc1d0f6b76d4681a82522f2b6e9e9200
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212495235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170ff500920bc13e16ff63ea47d0b338e8a7f3fe4bc37ec40ad24666c908bded`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:17:32 GMT
RUN groupadd -g 1001 mysql
# Tue, 12 Nov 2019 02:17:33 GMT
RUN useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:17:40 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release setup ps80
# Tue, 12 Nov 2019 02:17:40 GMT
ENV PERCONA_VERSION=8.0.16-7.1.el7
# Tue, 12 Nov 2019 02:18:45 GMT
RUN yum install -y 		percona-server-server-${PERCONA_VERSION} 		percona-server-tokudb-${PERCONA_VERSION} 		percona-server-rocksdb-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:18:46 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 12 Nov 2019 02:18:46 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:18:47 GMT
COPY file:98315a3cdd5c008868bca89eff8d9037073d3b25d79ce0bfce9220868c87243b in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:18:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:18:47 GMT
USER mysql
# Tue, 12 Nov 2019 02:18:47 GMT
EXPOSE 3306 33060
# Tue, 12 Nov 2019 02:18:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd87aed0b083cb1b639d2dd7663d85166a65b7f00423492d3fc893b46ba1efa1`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41c0be21edf06063e243b167324669066e08e5d4bd8b67f13875d6b3690c346`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc216c52e445aae86a60a1dd1d290b2bb31c001c827f7c8296fd28386dde5828`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 6.4 MB (6437188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851dfa885f2912de0bead50f3f1788ee494476faa2edb3439c7339bd5c921ba`  
		Last Modified: Tue, 12 Nov 2019 02:23:32 GMT  
		Size: 130.3 MB (130271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788672c6ab1554ba42ba03b003c232b97c4c9b4eceb9bf21b0f856f4536cf88`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd546236c6797e65a5d97a0c13fbdcad96d4eab143d0fbc1400d80b9cd85cf8`  
		Last Modified: Tue, 12 Nov 2019 02:23:06 GMT  
		Size: 3.1 KB (3068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:ps-8.0.16-7`

```console
$ docker pull percona@sha256:72f7e06c3929d6d2636a0f4d6d02bb117c8b3b0991491236a99b09783fca344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:ps-8.0.16-7` - linux; amd64

```console
$ docker pull percona@sha256:e442b0d658ae944c0144c04bb3e676b7bc1d0f6b76d4681a82522f2b6e9e9200
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212495235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170ff500920bc13e16ff63ea47d0b338e8a7f3fe4bc37ec40ad24666c908bded`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:17:32 GMT
RUN groupadd -g 1001 mysql
# Tue, 12 Nov 2019 02:17:33 GMT
RUN useradd -u 1001 -r -g 1001 -s /sbin/nologin 		-c "Default Application User" mysql
# Tue, 12 Nov 2019 02:17:40 GMT
RUN export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 	&& gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona 	&& rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7 	&& curl -L -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm 	&& rpmkeys --checksig /tmp/percona-release.rpm 	&& yum install -y /tmp/percona-release.rpm 	&& rm -rf "$GNUPGHOME" /tmp/percona-release.rpm 	&& rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY 	&& percona-release disable all 	&& percona-release setup ps80
# Tue, 12 Nov 2019 02:17:40 GMT
ENV PERCONA_VERSION=8.0.16-7.1.el7
# Tue, 12 Nov 2019 02:18:45 GMT
RUN yum install -y 		percona-server-server-${PERCONA_VERSION} 		percona-server-tokudb-${PERCONA_VERSION} 		percona-server-rocksdb-${PERCONA_VERSION} 		jemalloc 		which 		policycoreutils 	&& yum clean all 	&& rm -rf /var/cache/yum /var/lib/mysql
# Tue, 12 Nov 2019 02:18:46 GMT
RUN /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d 	&& find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/' 	&& echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf 	&& printf '[mysqld]\nskip-host-cache\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf 	&& /usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql 	&& echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql 	&& echo "THP_SETTING=never" >> /etc/sysconfig/mysql 	&& chown -R mysql:root /etc/my.cnf /etc/my.cnf.d 	&& chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d
# Tue, 12 Nov 2019 02:18:46 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 12 Nov 2019 02:18:47 GMT
COPY file:98315a3cdd5c008868bca89eff8d9037073d3b25d79ce0bfce9220868c87243b in /docker-entrypoint.sh 
# Tue, 12 Nov 2019 02:18:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Nov 2019 02:18:47 GMT
USER mysql
# Tue, 12 Nov 2019 02:18:47 GMT
EXPOSE 3306 33060
# Tue, 12 Nov 2019 02:18:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd87aed0b083cb1b639d2dd7663d85166a65b7f00423492d3fc893b46ba1efa1`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41c0be21edf06063e243b167324669066e08e5d4bd8b67f13875d6b3690c346`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.6 KB (1571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc216c52e445aae86a60a1dd1d290b2bb31c001c827f7c8296fd28386dde5828`  
		Last Modified: Tue, 12 Nov 2019 02:23:07 GMT  
		Size: 6.4 MB (6437188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851dfa885f2912de0bead50f3f1788ee494476faa2edb3439c7339bd5c921ba`  
		Last Modified: Tue, 12 Nov 2019 02:23:32 GMT  
		Size: 130.3 MB (130271020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6788672c6ab1554ba42ba03b003c232b97c4c9b4eceb9bf21b0f856f4536cf88`  
		Last Modified: Tue, 12 Nov 2019 02:23:05 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd546236c6797e65a5d97a0c13fbdcad96d4eab143d0fbc1400d80b9cd85cf8`  
		Last Modified: Tue, 12 Nov 2019 02:23:06 GMT  
		Size: 3.1 KB (3068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-3.6`

```console
$ docker pull percona@sha256:94895957a62955d506a0583f6622be02e242fc30d9b4ef93b88827425048ea45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-3.6` - linux; amd64

```console
$ docker pull percona@sha256:b54f88d0be5dcccd0276c8ba5c15e0c475e05991204dd325727b01410c7051bd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180210232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6191b90e11dbf2422550427bf427f48165967b97716bb7a42a29ff99eec636e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:21:45 GMT
RUN export GNUPGHOME="$(mktemp -d)"         && gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A         && gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona         && rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-1.0-7.noarch.rpm         && rpmkeys --checksig /tmp/percona-release.rpm         && yum install -y /tmp/percona-release.rpm         && rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY         && percona-release disable all         && percona-release enable original release
# Tue, 12 Nov 2019 02:21:46 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 12 Nov 2019 02:21:46 GMT
ENV PERCONA_MAJOR=36
# Tue, 12 Nov 2019 02:21:47 GMT
ENV PERCONA_VERSION=3.6.12-3.2.el7
# Tue, 12 Nov 2019 02:21:47 GMT
ENV K8S_TOOLS_VERSION=0.4.1
# Tue, 12 Nov 2019 02:22:47 GMT
RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm         && yum install -y                 Percona-Server-MongoDB-36-server-${PERCONA_VERSION}                 Percona-Server-MongoDB-36-mongos-${PERCONA_VERSION}                 Percona-Server-MongoDB-36-tools-${PERCONA_VERSION}                 Percona-Server-MongoDB-36-shell-${PERCONA_VERSION}                 curl                 jq         && yum clean all         && rm -rf /var/cache/yum /data/db  && mkdir -p /data/db         && chown -R 1001:0 /data/db
# Tue, 12 Nov 2019 02:22:49 GMT
RUN curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator     && curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck     && chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 12 Nov 2019 02:22:49 GMT
VOLUME [/data/db]
# Tue, 12 Nov 2019 02:22:49 GMT
COPY file:73b257e28d42d38a579e50c8dbd964c054f38728692627d5438a0aa11526970b in /entrypoint.sh 
# Tue, 12 Nov 2019 02:22:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Nov 2019 02:22:49 GMT
EXPOSE 27017
# Tue, 12 Nov 2019 02:22:50 GMT
USER 1001
# Tue, 12 Nov 2019 02:22:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c058f3c741ce5f904f9bf2fee41f0a4be04658d8a2e9fe22244823280e19726d`  
		Last Modified: Tue, 12 Nov 2019 02:24:55 GMT  
		Size: 6.4 MB (6441681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec444b2d5801d6dca858d6ff95c1047cc6b6086c2ab3e288378467bdbf216b0c`  
		Last Modified: Tue, 12 Nov 2019 02:24:54 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9468009357d5e128392fbb561ee4e13e4cea8b2e09e8229c397ef080c8e5063e`  
		Last Modified: Tue, 12 Nov 2019 02:25:09 GMT  
		Size: 91.7 MB (91682104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ed6c4a15e018b28ee2b706cb46acc6f020292394c4506141d5a5f1b35897f4`  
		Last Modified: Tue, 12 Nov 2019 02:24:54 GMT  
		Size: 6.3 MB (6300361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f9bb61c761464250bf3dcd9e80d5399a20846356557619f661ac49b6228fd`  
		Last Modified: Tue, 12 Nov 2019 02:24:53 GMT  
		Size: 3.8 KB (3810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-3.6.16`

**does not exist** (yet?)

## `percona:psmdb-4.0`

```console
$ docker pull percona@sha256:98913526cf85d0dc6d2a9f5b4a4ecc539db4e270abd59285e65a1f5ff862dc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-4.0` - linux; amd64

```console
$ docker pull percona@sha256:8f3f05470c88894fd3765dc4185155cd78dbc222403fb6f7bac44fc10dfd6e75
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183679563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd1efd057d483cf8f8819283c3c34d08768689a4c4d28e4aaecfc3e60890543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:17:31 GMT
MAINTAINER Percona Development <info@percona.com>
# Tue, 12 Nov 2019 02:20:31 GMT
RUN export GNUPGHOME="$(mktemp -d)"         && gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A         && gpg --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona         && rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7         && curl -L -o /tmp/percona-release.rpm https://repo.percona.com/percona/yum/percona-release-1.0-7.noarch.rpm         && rpmkeys --checksig /tmp/percona-release.rpm         && yum install -y /tmp/percona-release.rpm         && rm -rf "$GNUPGHOME" /tmp/percona-release.rpm         && rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY         && percona-release disable all         && percona-release enable psmdb-40 release
# Tue, 12 Nov 2019 02:20:32 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 12 Nov 2019 02:20:32 GMT
ENV PERCONA_MAJOR=40
# Tue, 12 Nov 2019 02:20:32 GMT
ENV PERCONA_VERSION=4.0.10-5.el7
# Tue, 12 Nov 2019 02:20:32 GMT
ENV K8S_TOOLS_VERSION=0.4.1
# Tue, 12 Nov 2019 02:21:32 GMT
RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm         && yum install -y                 percona-server-mongodb-server-${PERCONA_VERSION}                 percona-server-mongodb-mongos-${PERCONA_VERSION}                 percona-server-mongodb-shell-${PERCONA_VERSION}                 percona-server-mongodb-tools-${PERCONA_VERSION}                 curl                 jq         && yum clean all         && rm -rf /var/cache/yum /data/db  && mkdir -p /data/db         && chown -R 1001:0 /data/db
# Tue, 12 Nov 2019 02:21:34 GMT
RUN curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator     && curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck     && chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 12 Nov 2019 02:21:34 GMT
VOLUME [/data/db]
# Tue, 12 Nov 2019 02:21:34 GMT
COPY file:73b257e28d42d38a579e50c8dbd964c054f38728692627d5438a0aa11526970b in /entrypoint.sh 
# Tue, 12 Nov 2019 02:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Nov 2019 02:21:35 GMT
EXPOSE 27017
# Tue, 12 Nov 2019 02:21:35 GMT
USER 1001
# Tue, 12 Nov 2019 02:21:35 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20934d020c32ca2297a6a7246a2889224b009113a9fba755afd6756fd1c72c38`  
		Last Modified: Tue, 12 Nov 2019 02:24:31 GMT  
		Size: 6.4 MB (6441697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e40f0510413a6b633833f2537acc7e08d4d2aabfcb067b6bdf0cd9e1d8ed488`  
		Last Modified: Tue, 12 Nov 2019 02:24:29 GMT  
		Size: 1.6 KB (1562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5648ec676cde34e1f50d69bf625f5bad96c1108104a53884c15bb171897096`  
		Last Modified: Tue, 12 Nov 2019 02:24:49 GMT  
		Size: 95.2 MB (95151411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b73b31385e25b49493f96f712db06588b124de5d7e11805053fa6f7fde96d6`  
		Last Modified: Tue, 12 Nov 2019 02:24:30 GMT  
		Size: 6.3 MB (6300372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2247e98a4cefad39e8f7fe6c867635b2f033d9131cfd5a7b02dbafe3a11b591`  
		Last Modified: Tue, 12 Nov 2019 02:24:29 GMT  
		Size: 3.8 KB (3809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `percona:psmdb-4.0.14`

**does not exist** (yet?)
