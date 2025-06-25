## `percona:ps-8.0.42-33`

```console
$ docker pull percona@sha256:d82448a41d5a34a3a70bc99cf470c77a4d2a702dec40aa27d0c62622421671d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.42-33` - linux; amd64

```console
$ docker pull percona@sha256:fc2e2b10d2a4ed697dc4006b62e2fd7ce4e974668a373f082a139ea8fa2c8176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431014670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9d90b6d5d2dbec59e4ed0032c1392a283bd32aff353f2cf8abaad47b63345e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 19 May 2025 11:07:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 May 2025 11:07:08 GMT
LABEL url="https://www.redhat.com"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 19 May 2025 11:07:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 May 2025 11:07:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 May 2025 11:07:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 May 2025 11:07:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 May 2025 11:07:08 GMT
ENV container oci
# Mon, 19 May 2025 11:07:08 GMT
COPY dir:9f1e3d7980aa1b8b007cf8dcf05575fff696655332be09ae87c8f7de7f00e923 in / 
# Mon, 19 May 2025 11:07:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 19 May 2025 11:07:08 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 11:07:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Mon, 19 May 2025 11:07:08 GMT
LABEL "build-date"="2025-06-24T16:31:57" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Mon, 19 May 2025 11:07:08 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 19 May 2025 11:07:08 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_VERSION=8.0.42-33.1
# Mon, 19 May 2025 11:07:08 GMT
ENV MYSQL_SHELL_VERSION=8.0.42-1
# Mon, 19 May 2025 11:07:08 GMT
ENV OS_VER=el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_PERCONA_VERSION=8.0.42-33.1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.42-1.el9
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_REPO=testing
# Mon, 19 May 2025 11:07:08 GMT
ENV PS_TELEMETRY_VERSION=8.0.42-33-1
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 19 May 2025 11:07:08 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 19 May 2025 11:07:08 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Mon, 19 May 2025 11:07:08 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Mon, 19 May 2025 11:07:08 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 19 May 2025 11:07:08 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 11:07:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 11:07:08 GMT
USER mysql
# Mon, 19 May 2025 11:07:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 19 May 2025 11:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7073092d8bcd7b6d72345cfa87d8389a33f629b3c49ff887ad3a51c6ed8dfd83`  
		Last Modified: Tue, 24 Jun 2025 18:09:29 GMT  
		Size: 39.7 MB (39650665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac85605fc3b3fb8a56768de71f7a660c7ef49ee772943bba7a4ca690f1336fd`  
		Last Modified: Wed, 25 Jun 2025 18:08:53 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff36882d12a17263981cc8f7cf02b7de6d9ba2a298a94f1eb8beff96391046f`  
		Last Modified: Wed, 25 Jun 2025 20:10:40 GMT  
		Size: 8.8 MB (8847343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b059ad5dabf1b776b3e2307243e26e09054feff9805de3ee76c0db87b6a0b18`  
		Last Modified: Wed, 25 Jun 2025 20:11:18 GMT  
		Size: 382.5 MB (382506928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51caceec5590bdcfb32fc2045b012b76dc889d71d7b5f2403f86021f773baa1`  
		Last Modified: Wed, 25 Jun 2025 18:09:05 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213d9741a1d414a148796f83344318303c7bb093903b99bb12adec4c41a17908`  
		Last Modified: Wed, 25 Jun 2025 18:09:10 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300735b0db8c22ca58be18b6576dcc16e4623d8a935fb2911a25e38fa96ba239`  
		Last Modified: Wed, 25 Jun 2025 18:00:06 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.42-33` - unknown; unknown

```console
$ docker pull percona@sha256:cd452d1f6b85550aeab4f29b71b6b74eb01e3b3911e52ca63a7582ca2e7ddb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751e1baa1c43ad59fee03cf62eb6455861eaf1f410287782d09491a3e512602f`

```dockerfile
```

-	Layers:
	-	`sha256:9a7c9e2c6af7f637b9dcdbdeac9fa36a1846b34c480d68683f976ccab587baa6`  
		Last Modified: Wed, 25 Jun 2025 20:10:38 GMT  
		Size: 30.8 KB (30848 bytes)  
		MIME: application/vnd.in-toto+json
