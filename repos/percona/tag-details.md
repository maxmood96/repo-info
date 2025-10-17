<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `percona`

-	[`percona:8`](#percona8)
-	[`percona:8-centos`](#percona8-centos)
-	[`percona:8.0`](#percona80)
-	[`percona:8.0-centos`](#percona80-centos)
-	[`percona:8.0.43-34`](#percona8043-34)
-	[`percona:8.0.43-34-centos`](#percona8043-34-centos)
-	[`percona:ps-8`](#perconaps-8)
-	[`percona:ps-8.0`](#perconaps-80)
-	[`percona:ps-8.0.43-34`](#perconaps-8043-34)
-	[`percona:psmdb-6.0`](#perconapsmdb-60)
-	[`percona:psmdb-6.0.25`](#perconapsmdb-6025)
-	[`percona:psmdb-7.0`](#perconapsmdb-70)
-	[`percona:psmdb-7.0.24`](#perconapsmdb-7024)
-	[`percona:psmdb-8.0`](#perconapsmdb-80)
-	[`percona:psmdb-8.0.12`](#perconapsmdb-8012)

## `percona:8`

```console
$ docker pull percona@sha256:670e00bfc2d8c71851910abb2430051a4ef8f6e41e0c8ed68087d54d8e89d32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8` - linux; amd64

```console
$ docker pull percona@sha256:8888407d765074366bd6db8189c9df2915e3e05647a22d3e6aff26e758c41f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410809819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51453e5dc0ea304693538067a2f5a7430f64bcf7ef9da214e7afc002d460958`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed647dc2fc40c3c50aed07ae5c90493c03952dda7de21ce7cc705150c4dcc583`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f27424d0eb3c8ff9411252193fd88c1ed5f94182bbb7e40296432e0bbaaeab`  
		Last Modified: Thu, 16 Oct 2025 19:27:16 GMT  
		Size: 8.8 MB (8764747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecea2d11c790664bb36331b3108f9741869b1998aaf650926b3faffb9113a53`  
		Last Modified: Thu, 16 Oct 2025 20:12:49 GMT  
		Size: 362.4 MB (362381811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7305b2ab62ba75f6f567626262a34c67207dd427d85b93e02dc021f989fd5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75b9f6d6a696b2cfb85100468b0377346a808f021bffef7e4b1ab40e1f70a6`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d8b7dee41c02b258d284884b1be12c91a48efc24fa073dc15a06c07e76d876`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8` - unknown; unknown

```console
$ docker pull percona@sha256:fa8e77d86d0e27f0b53e8272de596028445a7a5d23fb977ffae3db11e3dd0b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe56185f8f3993be5053d31a98541925684bb5918c4bf801cb31414958ef47b`

```dockerfile
```

-	Layers:
	-	`sha256:20620edd107047150beedef12e8e6649e2cefb1a55c512c39388ecd03c766c6e`  
		Last Modified: Thu, 16 Oct 2025 23:10:19 GMT  
		Size: 30.9 KB (30890 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8-centos`

```console
$ docker pull percona@sha256:670e00bfc2d8c71851910abb2430051a4ef8f6e41e0c8ed68087d54d8e89d32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8-centos` - linux; amd64

```console
$ docker pull percona@sha256:8888407d765074366bd6db8189c9df2915e3e05647a22d3e6aff26e758c41f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410809819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51453e5dc0ea304693538067a2f5a7430f64bcf7ef9da214e7afc002d460958`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed647dc2fc40c3c50aed07ae5c90493c03952dda7de21ce7cc705150c4dcc583`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f27424d0eb3c8ff9411252193fd88c1ed5f94182bbb7e40296432e0bbaaeab`  
		Last Modified: Thu, 16 Oct 2025 19:27:16 GMT  
		Size: 8.8 MB (8764747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecea2d11c790664bb36331b3108f9741869b1998aaf650926b3faffb9113a53`  
		Last Modified: Thu, 16 Oct 2025 20:12:49 GMT  
		Size: 362.4 MB (362381811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7305b2ab62ba75f6f567626262a34c67207dd427d85b93e02dc021f989fd5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75b9f6d6a696b2cfb85100468b0377346a808f021bffef7e4b1ab40e1f70a6`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d8b7dee41c02b258d284884b1be12c91a48efc24fa073dc15a06c07e76d876`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8-centos` - unknown; unknown

```console
$ docker pull percona@sha256:fa8e77d86d0e27f0b53e8272de596028445a7a5d23fb977ffae3db11e3dd0b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe56185f8f3993be5053d31a98541925684bb5918c4bf801cb31414958ef47b`

```dockerfile
```

-	Layers:
	-	`sha256:20620edd107047150beedef12e8e6649e2cefb1a55c512c39388ecd03c766c6e`  
		Last Modified: Thu, 16 Oct 2025 23:10:19 GMT  
		Size: 30.9 KB (30890 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0`

```console
$ docker pull percona@sha256:670e00bfc2d8c71851910abb2430051a4ef8f6e41e0c8ed68087d54d8e89d32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0` - linux; amd64

```console
$ docker pull percona@sha256:8888407d765074366bd6db8189c9df2915e3e05647a22d3e6aff26e758c41f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410809819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51453e5dc0ea304693538067a2f5a7430f64bcf7ef9da214e7afc002d460958`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed647dc2fc40c3c50aed07ae5c90493c03952dda7de21ce7cc705150c4dcc583`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f27424d0eb3c8ff9411252193fd88c1ed5f94182bbb7e40296432e0bbaaeab`  
		Last Modified: Thu, 16 Oct 2025 19:27:16 GMT  
		Size: 8.8 MB (8764747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecea2d11c790664bb36331b3108f9741869b1998aaf650926b3faffb9113a53`  
		Last Modified: Thu, 16 Oct 2025 20:12:49 GMT  
		Size: 362.4 MB (362381811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7305b2ab62ba75f6f567626262a34c67207dd427d85b93e02dc021f989fd5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75b9f6d6a696b2cfb85100468b0377346a808f021bffef7e4b1ab40e1f70a6`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d8b7dee41c02b258d284884b1be12c91a48efc24fa073dc15a06c07e76d876`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0` - unknown; unknown

```console
$ docker pull percona@sha256:fa8e77d86d0e27f0b53e8272de596028445a7a5d23fb977ffae3db11e3dd0b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe56185f8f3993be5053d31a98541925684bb5918c4bf801cb31414958ef47b`

```dockerfile
```

-	Layers:
	-	`sha256:20620edd107047150beedef12e8e6649e2cefb1a55c512c39388ecd03c766c6e`  
		Last Modified: Thu, 16 Oct 2025 23:10:19 GMT  
		Size: 30.9 KB (30890 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0-centos`

```console
$ docker pull percona@sha256:670e00bfc2d8c71851910abb2430051a4ef8f6e41e0c8ed68087d54d8e89d32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0-centos` - linux; amd64

```console
$ docker pull percona@sha256:8888407d765074366bd6db8189c9df2915e3e05647a22d3e6aff26e758c41f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410809819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51453e5dc0ea304693538067a2f5a7430f64bcf7ef9da214e7afc002d460958`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed647dc2fc40c3c50aed07ae5c90493c03952dda7de21ce7cc705150c4dcc583`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f27424d0eb3c8ff9411252193fd88c1ed5f94182bbb7e40296432e0bbaaeab`  
		Last Modified: Thu, 16 Oct 2025 19:27:16 GMT  
		Size: 8.8 MB (8764747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecea2d11c790664bb36331b3108f9741869b1998aaf650926b3faffb9113a53`  
		Last Modified: Thu, 16 Oct 2025 20:12:49 GMT  
		Size: 362.4 MB (362381811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7305b2ab62ba75f6f567626262a34c67207dd427d85b93e02dc021f989fd5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75b9f6d6a696b2cfb85100468b0377346a808f021bffef7e4b1ab40e1f70a6`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d8b7dee41c02b258d284884b1be12c91a48efc24fa073dc15a06c07e76d876`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0-centos` - unknown; unknown

```console
$ docker pull percona@sha256:fa8e77d86d0e27f0b53e8272de596028445a7a5d23fb977ffae3db11e3dd0b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe56185f8f3993be5053d31a98541925684bb5918c4bf801cb31414958ef47b`

```dockerfile
```

-	Layers:
	-	`sha256:20620edd107047150beedef12e8e6649e2cefb1a55c512c39388ecd03c766c6e`  
		Last Modified: Thu, 16 Oct 2025 23:10:19 GMT  
		Size: 30.9 KB (30890 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.43-34`

```console
$ docker pull percona@sha256:670e00bfc2d8c71851910abb2430051a4ef8f6e41e0c8ed68087d54d8e89d32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.43-34` - linux; amd64

```console
$ docker pull percona@sha256:8888407d765074366bd6db8189c9df2915e3e05647a22d3e6aff26e758c41f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410809819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51453e5dc0ea304693538067a2f5a7430f64bcf7ef9da214e7afc002d460958`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed647dc2fc40c3c50aed07ae5c90493c03952dda7de21ce7cc705150c4dcc583`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f27424d0eb3c8ff9411252193fd88c1ed5f94182bbb7e40296432e0bbaaeab`  
		Last Modified: Thu, 16 Oct 2025 19:27:16 GMT  
		Size: 8.8 MB (8764747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecea2d11c790664bb36331b3108f9741869b1998aaf650926b3faffb9113a53`  
		Last Modified: Thu, 16 Oct 2025 20:12:49 GMT  
		Size: 362.4 MB (362381811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7305b2ab62ba75f6f567626262a34c67207dd427d85b93e02dc021f989fd5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75b9f6d6a696b2cfb85100468b0377346a808f021bffef7e4b1ab40e1f70a6`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d8b7dee41c02b258d284884b1be12c91a48efc24fa073dc15a06c07e76d876`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.43-34` - unknown; unknown

```console
$ docker pull percona@sha256:fa8e77d86d0e27f0b53e8272de596028445a7a5d23fb977ffae3db11e3dd0b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe56185f8f3993be5053d31a98541925684bb5918c4bf801cb31414958ef47b`

```dockerfile
```

-	Layers:
	-	`sha256:20620edd107047150beedef12e8e6649e2cefb1a55c512c39388ecd03c766c6e`  
		Last Modified: Thu, 16 Oct 2025 23:10:19 GMT  
		Size: 30.9 KB (30890 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:8.0.43-34-centos`

```console
$ docker pull percona@sha256:670e00bfc2d8c71851910abb2430051a4ef8f6e41e0c8ed68087d54d8e89d32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:8.0.43-34-centos` - linux; amd64

```console
$ docker pull percona@sha256:8888407d765074366bd6db8189c9df2915e3e05647a22d3e6aff26e758c41f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410809819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51453e5dc0ea304693538067a2f5a7430f64bcf7ef9da214e7afc002d460958`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed647dc2fc40c3c50aed07ae5c90493c03952dda7de21ce7cc705150c4dcc583`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f27424d0eb3c8ff9411252193fd88c1ed5f94182bbb7e40296432e0bbaaeab`  
		Last Modified: Thu, 16 Oct 2025 19:27:16 GMT  
		Size: 8.8 MB (8764747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecea2d11c790664bb36331b3108f9741869b1998aaf650926b3faffb9113a53`  
		Last Modified: Thu, 16 Oct 2025 20:12:49 GMT  
		Size: 362.4 MB (362381811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7305b2ab62ba75f6f567626262a34c67207dd427d85b93e02dc021f989fd5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75b9f6d6a696b2cfb85100468b0377346a808f021bffef7e4b1ab40e1f70a6`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d8b7dee41c02b258d284884b1be12c91a48efc24fa073dc15a06c07e76d876`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:8.0.43-34-centos` - unknown; unknown

```console
$ docker pull percona@sha256:fa8e77d86d0e27f0b53e8272de596028445a7a5d23fb977ffae3db11e3dd0b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe56185f8f3993be5053d31a98541925684bb5918c4bf801cb31414958ef47b`

```dockerfile
```

-	Layers:
	-	`sha256:20620edd107047150beedef12e8e6649e2cefb1a55c512c39388ecd03c766c6e`  
		Last Modified: Thu, 16 Oct 2025 23:10:19 GMT  
		Size: 30.9 KB (30890 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8`

```console
$ docker pull percona@sha256:670e00bfc2d8c71851910abb2430051a4ef8f6e41e0c8ed68087d54d8e89d32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8` - linux; amd64

```console
$ docker pull percona@sha256:8888407d765074366bd6db8189c9df2915e3e05647a22d3e6aff26e758c41f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410809819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51453e5dc0ea304693538067a2f5a7430f64bcf7ef9da214e7afc002d460958`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed647dc2fc40c3c50aed07ae5c90493c03952dda7de21ce7cc705150c4dcc583`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f27424d0eb3c8ff9411252193fd88c1ed5f94182bbb7e40296432e0bbaaeab`  
		Last Modified: Thu, 16 Oct 2025 19:27:16 GMT  
		Size: 8.8 MB (8764747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecea2d11c790664bb36331b3108f9741869b1998aaf650926b3faffb9113a53`  
		Last Modified: Thu, 16 Oct 2025 20:12:49 GMT  
		Size: 362.4 MB (362381811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7305b2ab62ba75f6f567626262a34c67207dd427d85b93e02dc021f989fd5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75b9f6d6a696b2cfb85100468b0377346a808f021bffef7e4b1ab40e1f70a6`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d8b7dee41c02b258d284884b1be12c91a48efc24fa073dc15a06c07e76d876`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8` - unknown; unknown

```console
$ docker pull percona@sha256:fa8e77d86d0e27f0b53e8272de596028445a7a5d23fb977ffae3db11e3dd0b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe56185f8f3993be5053d31a98541925684bb5918c4bf801cb31414958ef47b`

```dockerfile
```

-	Layers:
	-	`sha256:20620edd107047150beedef12e8e6649e2cefb1a55c512c39388ecd03c766c6e`  
		Last Modified: Thu, 16 Oct 2025 23:10:19 GMT  
		Size: 30.9 KB (30890 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0`

```console
$ docker pull percona@sha256:670e00bfc2d8c71851910abb2430051a4ef8f6e41e0c8ed68087d54d8e89d32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0` - linux; amd64

```console
$ docker pull percona@sha256:8888407d765074366bd6db8189c9df2915e3e05647a22d3e6aff26e758c41f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410809819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51453e5dc0ea304693538067a2f5a7430f64bcf7ef9da214e7afc002d460958`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed647dc2fc40c3c50aed07ae5c90493c03952dda7de21ce7cc705150c4dcc583`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f27424d0eb3c8ff9411252193fd88c1ed5f94182bbb7e40296432e0bbaaeab`  
		Last Modified: Thu, 16 Oct 2025 19:27:16 GMT  
		Size: 8.8 MB (8764747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecea2d11c790664bb36331b3108f9741869b1998aaf650926b3faffb9113a53`  
		Last Modified: Thu, 16 Oct 2025 20:12:49 GMT  
		Size: 362.4 MB (362381811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7305b2ab62ba75f6f567626262a34c67207dd427d85b93e02dc021f989fd5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75b9f6d6a696b2cfb85100468b0377346a808f021bffef7e4b1ab40e1f70a6`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d8b7dee41c02b258d284884b1be12c91a48efc24fa073dc15a06c07e76d876`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:fa8e77d86d0e27f0b53e8272de596028445a7a5d23fb977ffae3db11e3dd0b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe56185f8f3993be5053d31a98541925684bb5918c4bf801cb31414958ef47b`

```dockerfile
```

-	Layers:
	-	`sha256:20620edd107047150beedef12e8e6649e2cefb1a55c512c39388ecd03c766c6e`  
		Last Modified: Thu, 16 Oct 2025 23:10:19 GMT  
		Size: 30.9 KB (30890 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:ps-8.0.43-34`

```console
$ docker pull percona@sha256:670e00bfc2d8c71851910abb2430051a4ef8f6e41e0c8ed68087d54d8e89d32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.43-34` - linux; amd64

```console
$ docker pull percona@sha256:8888407d765074366bd6db8189c9df2915e3e05647a22d3e6aff26e758c41f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410809819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51453e5dc0ea304693538067a2f5a7430f64bcf7ef9da214e7afc002d460958`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 28 Aug 2025 09:34:52 GMT
ENV container oci
# Thu, 28 Aug 2025 09:34:52 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 28 Aug 2025 09:34:52 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 28 Aug 2025 09:34:52 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 28 Aug 2025 09:34:52 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_VERSION=8.0.43-34.1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV MYSQL_SHELL_VERSION=8.0.43-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV OS_VER=el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_PERCONA_VERSION=8.0.43-34.1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.43-1.el9
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_REPO=testing
# Thu, 28 Aug 2025 09:34:52 GMT
ENV PS_TELEMETRY_VERSION=8.0.43-34-1
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Thu, 28 Aug 2025 09:34:52 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_VERSION=0.1
# Thu, 28 Aug 2025 09:34:52 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Thu, 28 Aug 2025 09:34:52 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Thu, 28 Aug 2025 09:34:52 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 09:34:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 09:34:52 GMT
USER mysql
# Thu, 28 Aug 2025 09:34:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 28 Aug 2025 09:34:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed647dc2fc40c3c50aed07ae5c90493c03952dda7de21ce7cc705150c4dcc583`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f27424d0eb3c8ff9411252193fd88c1ed5f94182bbb7e40296432e0bbaaeab`  
		Last Modified: Thu, 16 Oct 2025 19:27:16 GMT  
		Size: 8.8 MB (8764747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecea2d11c790664bb36331b3108f9741869b1998aaf650926b3faffb9113a53`  
		Last Modified: Thu, 16 Oct 2025 20:12:49 GMT  
		Size: 362.4 MB (362381811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7305b2ab62ba75f6f567626262a34c67207dd427d85b93e02dc021f989fd5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75b9f6d6a696b2cfb85100468b0377346a808f021bffef7e4b1ab40e1f70a6`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d8b7dee41c02b258d284884b1be12c91a48efc24fa073dc15a06c07e76d876`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.43-34` - unknown; unknown

```console
$ docker pull percona@sha256:fa8e77d86d0e27f0b53e8272de596028445a7a5d23fb977ffae3db11e3dd0b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe56185f8f3993be5053d31a98541925684bb5918c4bf801cb31414958ef47b`

```dockerfile
```

-	Layers:
	-	`sha256:20620edd107047150beedef12e8e6649e2cefb1a55c512c39388ecd03c766c6e`  
		Last Modified: Thu, 16 Oct 2025 23:10:19 GMT  
		Size: 30.9 KB (30890 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:f7637802f11bfcf83fe03b586a4527387b351eb1796f588ca1cf18d395d29e72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:501d25e60229b7a7af73925fc42b79b8077ca05c2910c235beb14ac99dcac3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254060438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4065bb0ad92a4656e2f1cf498edd5cb35e0cfe844edd022c034d6287a6e31c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:26:55 GMT
ENV container oci
# Fri, 01 Aug 2025 11:26:55 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 01 Aug 2025 11:26:55 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_VERSION=6.0.25-20
# Fri, 01 Aug 2025 11:26:55 GMT
ENV OS_VER=el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV FULL_PERCONA_VERSION=6.0.25-20.el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_REPO=release
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 01 Aug 2025 11:26:55 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
VOLUME [/data/db]
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 01 Aug 2025 11:26:55 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Aug 2025 11:26:55 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 01 Aug 2025 11:26:55 GMT
USER 1001
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0971d255497469d093a54a7fbf3f6fb35ec433649ae1f5a0b160320b9a3290d`  
		Last Modified: Thu, 16 Oct 2025 19:27:17 GMT  
		Size: 8.4 MB (8395932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1712c28a52083944a7de810e8cdf8071d0950d70ddb15e35c7ce2739d50687f1`  
		Last Modified: Thu, 16 Oct 2025 23:11:07 GMT  
		Size: 205.1 MB (205058137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acbf9600f259ea91dccba2ca5cd69033af8df6301983a1f73e646bcb8a692e5`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba96ac3ce7b0f2c521202300b8a80541ebab4af82d7ebb27e988ee9a51265114`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c552db3238aa4c5b05a922fb6c541f6876b5984efc7de1924db3ba777f13d5e5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f22e3806828979064da80e3bbddb9b7753fec5f751b845788720aec9526a190`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f3d23fbde43f9d4ff9b120bf967cff670b2fc9c59fdc69992a0a9ed9651a61`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ccf9b40d441f1e41d395ec5d0e5eb358b5ad4fb2316edb99cc4903fd151a8c`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c00ce65c4e1a6fe41d8e2ebe30a85479401387b0b7191c2461e8f02b207a04`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0` - unknown; unknown

```console
$ docker pull percona@sha256:04759dc7bf69c8c5bef17c523b2705865b678429fca117435efb03fd79628ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3624cfb65bcc3fffb2e901e33b9bfb046ea56f6b24d26539a7a22d8d482ea0`

```dockerfile
```

-	Layers:
	-	`sha256:86e55870ac8106299bdf4863ad21ac10bb49f2ea6c912c02777cd47a14933b9f`  
		Last Modified: Thu, 16 Oct 2025 23:10:37 GMT  
		Size: 32.8 KB (32821 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-6.0.25`

```console
$ docker pull percona@sha256:f7637802f11bfcf83fe03b586a4527387b351eb1796f588ca1cf18d395d29e72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-6.0.25` - linux; amd64

```console
$ docker pull percona@sha256:501d25e60229b7a7af73925fc42b79b8077ca05c2910c235beb14ac99dcac3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254060438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4065bb0ad92a4656e2f1cf498edd5cb35e0cfe844edd022c034d6287a6e31c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:26:55 GMT
ENV container oci
# Fri, 01 Aug 2025 11:26:55 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Fri, 01 Aug 2025 11:26:55 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Fri, 01 Aug 2025 11:26:55 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 01 Aug 2025 11:26:55 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     gpg --batch --export --armor 3E6D826D3FBAB389C2F38E34BC4D06A08D8B756F > ${GNUPGHOME}/RPM-GPG-KEY-oracle;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9 ${GNUPGHOME}/RPM-GPG-KEY-oracle;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_VERSION=6.0.25-20
# Fri, 01 Aug 2025 11:26:55 GMT
ENV OS_VER=el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV FULL_PERCONA_VERSION=6.0.25-20.el9
# Fri, 01 Aug 2025 11:26:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 01 Aug 2025 11:26:55 GMT
ENV PSMDB_REPO=release
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_VERSION=0.1
# Fri, 01 Aug 2025 11:26:55 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
VOLUME [/data/db]
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Fri, 01 Aug 2025 11:26:55 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:26:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Aug 2025 11:26:55 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 01 Aug 2025 11:26:55 GMT
USER 1001
# Fri, 01 Aug 2025 11:26:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0971d255497469d093a54a7fbf3f6fb35ec433649ae1f5a0b160320b9a3290d`  
		Last Modified: Thu, 16 Oct 2025 19:27:17 GMT  
		Size: 8.4 MB (8395932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1712c28a52083944a7de810e8cdf8071d0950d70ddb15e35c7ce2739d50687f1`  
		Last Modified: Thu, 16 Oct 2025 23:11:07 GMT  
		Size: 205.1 MB (205058137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acbf9600f259ea91dccba2ca5cd69033af8df6301983a1f73e646bcb8a692e5`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 1.7 KB (1669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba96ac3ce7b0f2c521202300b8a80541ebab4af82d7ebb27e988ee9a51265114`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 4.1 KB (4072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c552db3238aa4c5b05a922fb6c541f6876b5984efc7de1924db3ba777f13d5e5`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f22e3806828979064da80e3bbddb9b7753fec5f751b845788720aec9526a190`  
		Last Modified: Thu, 16 Oct 2025 19:27:15 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f3d23fbde43f9d4ff9b120bf967cff670b2fc9c59fdc69992a0a9ed9651a61`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ccf9b40d441f1e41d395ec5d0e5eb358b5ad4fb2316edb99cc4903fd151a8c`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c00ce65c4e1a6fe41d8e2ebe30a85479401387b0b7191c2461e8f02b207a04`  
		Last Modified: Thu, 16 Oct 2025 19:27:14 GMT  
		Size: 4.8 KB (4844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-6.0.25` - unknown; unknown

```console
$ docker pull percona@sha256:04759dc7bf69c8c5bef17c523b2705865b678429fca117435efb03fd79628ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3624cfb65bcc3fffb2e901e33b9bfb046ea56f6b24d26539a7a22d8d482ea0`

```dockerfile
```

-	Layers:
	-	`sha256:86e55870ac8106299bdf4863ad21ac10bb49f2ea6c912c02777cd47a14933b9f`  
		Last Modified: Thu, 16 Oct 2025 23:10:37 GMT  
		Size: 32.8 KB (32821 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0`

```console
$ docker pull percona@sha256:9db172c56f866e21e65d7b3153ba8b9421e26d081ce68cbcd269b7dc6ed7f791
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0` - linux; amd64

```console
$ docker pull percona@sha256:db6e694d2a8b977e28fb2efa8a44d3c1d1b5e751d7829ea709e7277b234aea88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276236683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee17ab877a70d34d92dc616d673baa3ce3bc4c3fb360096c30f3423d7655a426`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 13:56:56 GMT
ENV container oci
# Mon, 06 Oct 2025 13:56:56 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 06 Oct 2025 13:56:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_VERSION=7.0.24-13
# Mon, 06 Oct 2025 13:56:56 GMT
ENV OS_VER=el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV FULL_PERCONA_VERSION=7.0.24-13.el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_REPO=release
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 06 Oct 2025 13:56:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GOSU_VERSION=1.11
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
VOLUME [/data/db]
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 06 Oct 2025 13:56:56 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Oct 2025 13:56:56 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 13:56:56 GMT
USER 1001
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f86a7e67467e876b0c2780b46fa9567c7a40a5a444afb1443ab0235c4c2cc56`  
		Last Modified: Thu, 16 Oct 2025 19:26:45 GMT  
		Size: 8.4 MB (8391311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446df674548993866af8d8fa3d24e9c16985e7309aae2e5f0492e4f336eeef63`  
		Last Modified: Thu, 16 Oct 2025 19:27:24 GMT  
		Size: 227.2 MB (227238994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d3a71a80116d2a84022c4036ecdbc34f4edd53083c455a9ac88f3c17671c97`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b57edbc756a792d0fccb530cbac57e096ee73a88f01398185ef5926502e256`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff49394bb5543492cc465938b1f7b32380bebebf1d5ee6cfef677efbe6b13f9`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe84fcc657e230ea9364b42eba5e48ef00399cdc13fb2646d2a34a99001c9cb`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a42588488bab1ce250b044af72dd1c36f99ebafc173e11b6a4941def0bf7cdd`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2b5975335cb023f3d87500871ec2271e0e470c26806b99d524e4d377ce7995`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d4d4d049727efb7d5261e6ae193e4bab38472a3ee4738b56dccf678bc0133d`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0` - unknown; unknown

```console
$ docker pull percona@sha256:ad4cf5adbf8da7ce42a11ede6fcf684878b0a544457bba62bbce839c0a295aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb04859a9c5f61ad7a61367f1bdc9a3d44f3c74e47ab47e8555edebec9ffb4e`

```dockerfile
```

-	Layers:
	-	`sha256:d7700481d4fca26b7a40d60160535bcf35b3b4cec4154c44b0c9c0be91723083`  
		Last Modified: Thu, 16 Oct 2025 23:10:43 GMT  
		Size: 32.3 KB (32328 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-7.0.24`

```console
$ docker pull percona@sha256:9db172c56f866e21e65d7b3153ba8b9421e26d081ce68cbcd269b7dc6ed7f791
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-7.0.24` - linux; amd64

```console
$ docker pull percona@sha256:db6e694d2a8b977e28fb2efa8a44d3c1d1b5e751d7829ea709e7277b234aea88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276236683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee17ab877a70d34d92dc616d673baa3ce3bc4c3fb360096c30f3423d7655a426`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 13:56:56 GMT
ENV container oci
# Mon, 06 Oct 2025 13:56:56 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 06 Oct 2025 13:56:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_VERSION=7.0.24-13
# Mon, 06 Oct 2025 13:56:56 GMT
ENV OS_VER=el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV FULL_PERCONA_VERSION=7.0.24-13.el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_REPO=release
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 06 Oct 2025 13:56:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-70 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-70/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GOSU_VERSION=1.11
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
VOLUME [/data/db]
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 06 Oct 2025 13:56:56 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Oct 2025 13:56:56 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 13:56:56 GMT
USER 1001
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f86a7e67467e876b0c2780b46fa9567c7a40a5a444afb1443ab0235c4c2cc56`  
		Last Modified: Thu, 16 Oct 2025 19:26:45 GMT  
		Size: 8.4 MB (8391311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446df674548993866af8d8fa3d24e9c16985e7309aae2e5f0492e4f336eeef63`  
		Last Modified: Thu, 16 Oct 2025 19:27:24 GMT  
		Size: 227.2 MB (227238994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d3a71a80116d2a84022c4036ecdbc34f4edd53083c455a9ac88f3c17671c97`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b57edbc756a792d0fccb530cbac57e096ee73a88f01398185ef5926502e256`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff49394bb5543492cc465938b1f7b32380bebebf1d5ee6cfef677efbe6b13f9`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe84fcc657e230ea9364b42eba5e48ef00399cdc13fb2646d2a34a99001c9cb`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 914.5 KB (914518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a42588488bab1ce250b044af72dd1c36f99ebafc173e11b6a4941def0bf7cdd`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2b5975335cb023f3d87500871ec2271e0e470c26806b99d524e4d377ce7995`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 4.0 KB (3960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d4d4d049727efb7d5261e6ae193e4bab38472a3ee4738b56dccf678bc0133d`  
		Last Modified: Thu, 16 Oct 2025 19:26:44 GMT  
		Size: 4.8 KB (4850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-7.0.24` - unknown; unknown

```console
$ docker pull percona@sha256:ad4cf5adbf8da7ce42a11ede6fcf684878b0a544457bba62bbce839c0a295aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 KB (32328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb04859a9c5f61ad7a61367f1bdc9a3d44f3c74e47ab47e8555edebec9ffb4e`

```dockerfile
```

-	Layers:
	-	`sha256:d7700481d4fca26b7a40d60160535bcf35b3b4cec4154c44b0c9c0be91723083`  
		Last Modified: Thu, 16 Oct 2025 23:10:43 GMT  
		Size: 32.3 KB (32328 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0`

```console
$ docker pull percona@sha256:39dbc583edec6a58b82b9f23b47607dfee02a72ec529e9611518cc0d7e9655cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0` - linux; amd64

```console
$ docker pull percona@sha256:15b45b89f3c38fc143cc28efb93091f67ed7040334597d1d6277503f9cd506a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291774187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6798f738d5c77d1946ea113979f37b63d7d48b9549e180315bd2099eec688d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 13:56:56 GMT
ENV container oci
# Mon, 06 Oct 2025 13:56:56 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 06 Oct 2025 13:56:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_VERSION=8.0.12-4
# Mon, 06 Oct 2025 13:56:56 GMT
ENV OS_VER=el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV FULL_PERCONA_VERSION=8.0.12-4.el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_REPO=testing
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 06 Oct 2025 13:56:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GOSU_VERSION=1.11
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
VOLUME [/data/db]
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 06 Oct 2025 13:56:56 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Oct 2025 13:56:56 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 13:56:56 GMT
USER 1001
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfc5ced32602c6cce2466c511555dc95d459a6930a07c7707a7a82592d1cf1c`  
		Last Modified: Thu, 16 Oct 2025 19:26:48 GMT  
		Size: 8.4 MB (8391239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99beb58a3909878b71b0f95234b6e94a08d7fee1c9ec7402480b31daa22f3063`  
		Last Modified: Thu, 16 Oct 2025 23:11:25 GMT  
		Size: 242.8 MB (242776578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b69c7f9d06d0486a4b6cdc7e93e3cdeba0af1e95720f0f281a8dd67cab69a6a`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a1a21176a09e883b28dc2a41a895771321e9d6be5d492444a714039bd112a`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3e70ce7edd347f3b06710259fe97fd71e51c58df462ef973f8c3ba86ffca99`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c0ffa3aedc10a930e4f4b765e6a23a816fb410b6d2990da0bf45bd833fad61`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 914.5 KB (914519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2035a26116fa6ca7dca74fb49e50f1b7b140561c098e1e2936a06c9dda398`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef752afd6582565a403764e5a84b7d800aa561aa76056fe612b43d2ecdb1859`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9103b540ae4e093627b0832735a8cd7802d507cea2e3e1c56c5548f7f40a7e56`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0` - unknown; unknown

```console
$ docker pull percona@sha256:ad37ac0aa4f8e9f50e6170305a27cecac5d6cb3b44f4a1852bbf118b5fc7e1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7888ad41be1f3e9da720d808fbdbb783a9d5fcab759f20c9266dccc53a3d5cfb`

```dockerfile
```

-	Layers:
	-	`sha256:a8aea2cac4e4c9b88c73fe821f546808c06ada9439d6ad9f3201f0dc1ae45746`  
		Last Modified: Thu, 16 Oct 2025 23:10:49 GMT  
		Size: 32.6 KB (32618 bytes)  
		MIME: application/vnd.in-toto+json

## `percona:psmdb-8.0.12`

```console
$ docker pull percona@sha256:39dbc583edec6a58b82b9f23b47607dfee02a72ec529e9611518cc0d7e9655cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:psmdb-8.0.12` - linux; amd64

```console
$ docker pull percona@sha256:15b45b89f3c38fc143cc28efb93091f67ed7040334597d1d6277503f9cd506a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291774187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6798f738d5c77d1946ea113979f37b63d7d48b9549e180315bd2099eec688d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 13:56:56 GMT
ENV container oci
# Mon, 06 Oct 2025 13:56:56 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 13:56:56 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 13:56:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 06 Oct 2025 13:56:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_VERSION=8.0.12-4
# Mon, 06 Oct 2025 13:56:56 GMT
ENV OS_VER=el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV FULL_PERCONA_VERSION=8.0.12-4.el9
# Mon, 06 Oct 2025 13:56:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV PSMDB_REPO=testing
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_VERSION=0.1
# Mon, 06 Oct 2025 13:56:56 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     percona-release enable psmdb-80 ${PSMDB_REPO};     microdnf -y update libgcrypt;     microdnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         numactl         numactl-libs         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         cyrus-sasl-plain         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-80/yum/${PSMDB_REPO}/9/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
COPY LICENSE /licenses/LICENSE.Dockerfile # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV GOSU_VERSION=1.11
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
VOLUME [/data/db]
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c - # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/percona/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown 1001:1001 /usr/local/percona # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Mon, 06 Oct 2025 13:56:56 GMT
COPY ps-entry-dockerhub.sh /entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:56:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Oct 2025 13:56:56 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 13:56:56 GMT
USER 1001
# Mon, 06 Oct 2025 13:56:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfc5ced32602c6cce2466c511555dc95d459a6930a07c7707a7a82592d1cf1c`  
		Last Modified: Thu, 16 Oct 2025 19:26:48 GMT  
		Size: 8.4 MB (8391239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99beb58a3909878b71b0f95234b6e94a08d7fee1c9ec7402480b31daa22f3063`  
		Last Modified: Thu, 16 Oct 2025 23:11:25 GMT  
		Size: 242.8 MB (242776578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b69c7f9d06d0486a4b6cdc7e93e3cdeba0af1e95720f0f281a8dd67cab69a6a`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 1.7 KB (1670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a1a21176a09e883b28dc2a41a895771321e9d6be5d492444a714039bd112a`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3e70ce7edd347f3b06710259fe97fd71e51c58df462ef973f8c3ba86ffca99`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c0ffa3aedc10a930e4f4b765e6a23a816fb410b6d2990da0bf45bd833fad61`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 914.5 KB (914519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2035a26116fa6ca7dca74fb49e50f1b7b140561c098e1e2936a06c9dda398`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef752afd6582565a403764e5a84b7d800aa561aa76056fe612b43d2ecdb1859`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 4.0 KB (3959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9103b540ae4e093627b0832735a8cd7802d507cea2e3e1c56c5548f7f40a7e56`  
		Last Modified: Thu, 16 Oct 2025 19:26:47 GMT  
		Size: 4.8 KB (4843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:psmdb-8.0.12` - unknown; unknown

```console
$ docker pull percona@sha256:ad37ac0aa4f8e9f50e6170305a27cecac5d6cb3b44f4a1852bbf118b5fc7e1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7888ad41be1f3e9da720d808fbdbb783a9d5fcab759f20c9266dccc53a3d5cfb`

```dockerfile
```

-	Layers:
	-	`sha256:a8aea2cac4e4c9b88c73fe821f546808c06ada9439d6ad9f3201f0dc1ae45746`  
		Last Modified: Thu, 16 Oct 2025 23:10:49 GMT  
		Size: 32.6 KB (32618 bytes)  
		MIME: application/vnd.in-toto+json
