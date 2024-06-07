## `mariadb:11-ubi`

```console
$ docker pull mariadb@sha256:40440199923ef00f855147aa6c1a1c991b535909f281f8b4343d4ec633f89217
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `mariadb:11-ubi` - linux; amd64

```console
$ docker pull mariadb@sha256:1d81e9318e537b06641ced695676ba5184fc1023cc1a0521b72d650a056632e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145460246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128b6f3192df146968b7522e4e81e6e19e1585ef3c8dde52be7a890c21e6fcf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 30 May 2024 13:35:45 GMT
ADD file:6b3c51c101388be0fae89df70c275c457df3109dd754e67aaa695ab57931a55a in / 
# Thu, 30 May 2024 13:35:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 30 May 2024 13:35:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 30 May 2024 13:35:46 GMT
ADD multi:10a5b9e3ab6a191968d4e9508eca8f1cb30ca8c8ff6681dd9ecbea964c42b6de in /etc/yum.repos.d/ 
# Thu, 30 May 2024 13:35:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 May 2024 13:35:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 30 May 2024 13:35:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 May 2024 13:35:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 May 2024 13:35:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 May 2024 13:35:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 May 2024 13:35:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 May 2024 13:35:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 May 2024 13:35:46 GMT
ENV container oci
# Thu, 30 May 2024 13:35:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 13:35:46 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 13:35:47 GMT
RUN rm -rf /var/log/*
# Thu, 30 May 2024 13:35:47 GMT
ADD file:2867968da940ee5c316f478f01298796b71b04357b6efbbbc1d7219d486e29b7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1717074713.json 
# Thu, 30 May 2024 13:35:47 GMT
ADD file:be47ef503ada1def84422c0f3cdaa00761a8066b1c6ebe894382ae45cbfaec35 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1717074713 
# Thu, 30 May 2024 13:35:47 GMT
LABEL "release"="949.1717074713" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-30T13:14:08" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1717074713"
# Thu, 30 May 2024 13:35:48 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3133872-373bc.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 30 May 2024 13:35:49 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 30 May 2024 13:35:50 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 30 May 2024 23:03:04 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 30 May 2024 23:03:04 GMT
ENV GOSU_VERSION=1.17
# Thu, 30 May 2024 23:03:04 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 30 May 2024 23:03:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 30 May 2024 23:03:04 GMT
ARG MARIADB_VERSION=11.4.2
# Thu, 30 May 2024 23:03:04 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-11.4.2 MariaDB-server-11.4.2 ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-11.4.2/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 30 May 2024 23:03:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 May 2024 23:03:04 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 May 2024 23:03:04 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 30 May 2024 23:03:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:428c4e67728c0398b6263211d375a9bebe8b3c56a76af661e5b3efe156886361`  
		Last Modified: Thu, 06 Jun 2024 08:39:56 GMT  
		Size: 38.9 MB (38880168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04fd829cc5b5872cbf425a5f965e07759733c8af20d7851580e398809f0dee3`  
		Last Modified: Fri, 07 Jun 2024 01:04:20 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef416d34263e5fc2ba94f7af98420fef3c0b22f188cc5544247df8abac18636`  
		Last Modified: Fri, 07 Jun 2024 01:04:20 GMT  
		Size: 983.5 KB (983470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dec77a27158cf7b41f1f6b3ce716c0ccefe71face355fe4d4c668ae055461dd`  
		Last Modified: Fri, 07 Jun 2024 01:04:20 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b504fbbd0ed8df73d21d0b269d8418b7a1967f3879891039d504f570ffc794`  
		Last Modified: Fri, 07 Jun 2024 01:04:20 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b244c887b38716498fcefcbbc4edc9e1565df593bd42d6f784e2a68b6b1102fa`  
		Last Modified: Fri, 07 Jun 2024 01:04:23 GMT  
		Size: 105.6 MB (105583064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e19df890f86da9ac320a8576f7ef622a10b1bf6bcde0950967f17c92cbf808`  
		Last Modified: Fri, 07 Jun 2024 01:04:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c883d859371303dec35a146f8cc320c195aa1f8dcb8fd94cf0fa5e89a74c0e9`  
		Last Modified: Fri, 07 Jun 2024 01:04:21 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a158dbbc49dbe905279010c050aefa112b01b2e8aab8fe0a037600210a6621`  
		Last Modified: Fri, 07 Jun 2024 01:04:21 GMT  
		Size: 8.3 KB (8339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:96e639441359c11ac2cc6d9f12c68d32da0fbc49f9dce38850c915cd8df8fc5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdee79fd8290b0e717a17c73e1cf6c4a274e26e8b4db1bd983ce1f5edb8cec4`

```dockerfile
```

-	Layers:
	-	`sha256:412a9c1ae5d41d3a0317e5a43e7781c60cae4df5884f67588ac9367d5580c21d`  
		Last Modified: Fri, 07 Jun 2024 01:04:20 GMT  
		Size: 3.9 MB (3884637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69c6dae3214b95d1a213c76b387d04b1caf40e8a2b6c0cad80fe8ff0f0a4989`  
		Last Modified: Fri, 07 Jun 2024 01:04:20 GMT  
		Size: 30.6 KB (30586 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8d5a7c48645528828842082087a6387ef2311a1ff2453b688d83fcf7e9a4335b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141974402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43dd0b10b37efd6ae36d60fc77683af6ed5f0dbc6a324d40dbe6a0edb6d8f05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 30 May 2024 13:35:31 GMT
ADD file:3b70ca75f887cc972d131fb5caf99fff1fcf1808900d6017705a3b6b5815c57f in / 
# Thu, 30 May 2024 13:35:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 30 May 2024 13:35:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 30 May 2024 13:35:32 GMT
ADD multi:10a5b9e3ab6a191968d4e9508eca8f1cb30ca8c8ff6681dd9ecbea964c42b6de in /etc/yum.repos.d/ 
# Thu, 30 May 2024 13:35:32 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 May 2024 13:35:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 30 May 2024 13:35:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 May 2024 13:35:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 May 2024 13:35:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 May 2024 13:35:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 May 2024 13:35:32 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 May 2024 13:35:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 May 2024 13:35:32 GMT
ENV container oci
# Thu, 30 May 2024 13:35:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 13:35:32 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 13:35:33 GMT
RUN rm -rf /var/log/*
# Thu, 30 May 2024 13:35:33 GMT
ADD file:0c56a50d30c503011b2cd2ad620c8b42e23f9a7b3209387c1ac85014ea8e51e8 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1717074713.json 
# Thu, 30 May 2024 13:35:33 GMT
ADD file:3a9c01c5d61ee0a5b80c728e4e882d1de507083d557a30843ff3cd99eda21cfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1717074713 
# Thu, 30 May 2024 13:35:33 GMT
LABEL "release"="949.1717074713" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-30T13:14:08" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1717074713"
# Thu, 30 May 2024 13:35:34 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3133872-373bc.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 30 May 2024 13:35:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 30 May 2024 13:35:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 30 May 2024 23:03:04 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 30 May 2024 23:03:04 GMT
ENV GOSU_VERSION=1.17
# Thu, 30 May 2024 23:03:04 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 30 May 2024 23:03:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 30 May 2024 23:03:04 GMT
ARG MARIADB_VERSION=11.4.2
# Thu, 30 May 2024 23:03:04 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-11.4.2 MariaDB-server-11.4.2 ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-11.4.2/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 30 May 2024 23:03:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 May 2024 23:03:04 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 May 2024 23:03:04 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 30 May 2024 23:03:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:2eb4a094086c55c8718178f8c03ee6268f662e2fe3ac281acbd7e5b4abd42768`  
		Last Modified: Thu, 06 Jun 2024 08:39:55 GMT  
		Size: 37.1 MB (37080678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4127750e4343f22b111d3522a60a6228090fdd7da3347493c990762955f44803`  
		Last Modified: Fri, 07 Jun 2024 05:54:55 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ec34908b631b65ecceeb62c1a1bd714ff4238cd8c5679288046e34f017230d`  
		Last Modified: Fri, 07 Jun 2024 05:54:55 GMT  
		Size: 913.8 KB (913803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7a1e82c9266f5790ffaaf62a6afaa01097410bf0e897e3fe370dab9edf7cfa`  
		Last Modified: Fri, 07 Jun 2024 05:54:55 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f3c9216712d87ea952bd55407960f9deb6dd6cda63a2609558218a8c8cb5af`  
		Last Modified: Fri, 07 Jun 2024 05:56:03 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216190f367788a8dae70ecc9625b0c4e3ac3b4a5cfdcb6445bb3db417eb73949`  
		Last Modified: Fri, 07 Jun 2024 05:56:07 GMT  
		Size: 104.0 MB (103966371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213dfb24aed7b62197e43f8e23d891a6947355dc90e77954599fe22da1530673`  
		Last Modified: Fri, 07 Jun 2024 05:56:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50486074707bdff102dbbb3a80cfc090eaac4dcc06a3371f1389fa8e11aa2aa5`  
		Last Modified: Fri, 07 Jun 2024 05:56:03 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf3e31d2099471a5a409dc86c5bbb2a50b9fdbaf2da36b482ace18b71fecc30`  
		Last Modified: Fri, 07 Jun 2024 05:56:04 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:a3f2f50367db606c2c923b6e8896236ff8fcc278235edcb3e31b0d3735f311bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bb79d3b99cb621e6589095e7a720c35efa19175304dfb8e480a2ccd8a40c8c`

```dockerfile
```

-	Layers:
	-	`sha256:04ebb73a9097de05663f50e7493061cdcc2afc4a8c0a8aa6148f8ca32909930c`  
		Last Modified: Fri, 07 Jun 2024 05:56:03 GMT  
		Size: 3.9 MB (3884469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a1ff4801ca95081ecc5a04040dc3eda51ed658d2a150094cc1f383d357e25e`  
		Last Modified: Fri, 07 Jun 2024 05:56:03 GMT  
		Size: 30.9 KB (30942 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:bf96695f200689fbb83f60cfb37abbe7816ad889c07bc1779a81040ba373a926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156002098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3690fad7728082b8a016cd3bdd14f854ff66c20d6454d34f671f3296bd83efb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 30 May 2024 13:35:34 GMT
ADD file:8a11e8afe4fad68b45b505db6ac31e944034f6abdc60d8fcf7f1cdf0da538039 in / 
# Thu, 30 May 2024 13:35:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 30 May 2024 13:35:36 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 30 May 2024 13:35:36 GMT
ADD multi:10a5b9e3ab6a191968d4e9508eca8f1cb30ca8c8ff6681dd9ecbea964c42b6de in /etc/yum.repos.d/ 
# Thu, 30 May 2024 13:35:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 May 2024 13:35:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 30 May 2024 13:35:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 May 2024 13:35:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 May 2024 13:35:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 May 2024 13:35:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 May 2024 13:35:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 May 2024 13:35:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 May 2024 13:35:36 GMT
ENV container oci
# Thu, 30 May 2024 13:35:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 13:35:36 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 13:35:37 GMT
RUN rm -rf /var/log/*
# Thu, 30 May 2024 13:35:37 GMT
ADD file:ed5945e6ebaf6348f1150110cab2c41219c5e559c36670f43bdb732b8876972d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1717074713.json 
# Thu, 30 May 2024 13:35:38 GMT
ADD file:40f6a258d8800b05b75117f66c0badee4ba1b750d7c01f88a1d2eb56a09c0bfc in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1717074713 
# Thu, 30 May 2024 13:35:38 GMT
LABEL "release"="949.1717074713" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-30T13:14:08" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1717074713"
# Thu, 30 May 2024 13:35:39 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3133872-373bc.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 30 May 2024 13:35:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 30 May 2024 13:35:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 30 May 2024 23:03:04 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 30 May 2024 23:03:04 GMT
ENV GOSU_VERSION=1.17
# Thu, 30 May 2024 23:03:04 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 30 May 2024 23:03:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 30 May 2024 23:03:04 GMT
ARG MARIADB_VERSION=11.4.2
# Thu, 30 May 2024 23:03:04 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-11.4.2 MariaDB-server-11.4.2 ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-11.4.2/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 30 May 2024 23:03:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 May 2024 23:03:04 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 May 2024 23:03:04 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 30 May 2024 23:03:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e3f06c9962057a5cc6e14b55583c5cc376f23326466b1686e09163bcfed6781b`  
		Last Modified: Thu, 06 Jun 2024 18:11:46 GMT  
		Size: 43.4 MB (43361533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030ec01d3ee64db0f6698fbe418d602d35a68cb726d3d0f00c05af677ccc21c4`  
		Last Modified: Fri, 07 Jun 2024 04:31:17 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776a21848f1081f3c5a9b7c7065e4aa3a4dec681ef217a0c16bed2c5626353a`  
		Last Modified: Fri, 07 Jun 2024 04:31:18 GMT  
		Size: 904.3 KB (904317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc4a6ccf8bfaa037c7efad6a084b202efbc01a1dbc8311e9a5df624102ac5e7`  
		Last Modified: Fri, 07 Jun 2024 04:31:17 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db9d09bb27ee30cb99d92a149ad7ffba937beba30df8b1b8102d01e3ba709e6`  
		Last Modified: Fri, 07 Jun 2024 04:38:08 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1ca58e72c1c6412f19f9ac558db6987a8253f618c69984d6d054e37e6fdde3`  
		Last Modified: Fri, 07 Jun 2024 04:38:12 GMT  
		Size: 111.7 MB (111722693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b0f2b7e43fec7a13d633cf339931957104592e7eb0f9b23d7effe0b7b65016`  
		Last Modified: Fri, 07 Jun 2024 04:38:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0e68c5fa36791d3007b2148ce129be3c2b21fa53f7959b6afcc5483034843`  
		Last Modified: Fri, 07 Jun 2024 04:38:08 GMT  
		Size: 3.6 KB (3618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e76424304211531bd91e70c4dcea498d0c1bec68fbf7e09d1537b7e4fa3891`  
		Last Modified: Fri, 07 Jun 2024 04:38:09 GMT  
		Size: 8.3 KB (8343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:a050b9f323b7831540c04d941c6109d56b07788c6927dba454db7c26c080e5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857a1fe287a586a7ed66afb03f99f29d085993f87e889412d49ef53fee95edb7`

```dockerfile
```

-	Layers:
	-	`sha256:ed54ffe2c687064c07deb3ddbf71e094b7fc65edbda9824b55fa54f91e74aa3d`  
		Last Modified: Fri, 07 Jun 2024 04:38:08 GMT  
		Size: 3.9 MB (3885662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f971889e277e8601238f39e16f4b65c48fd859be8560982dedab168fb1ef0e`  
		Last Modified: Fri, 07 Jun 2024 04:38:08 GMT  
		Size: 30.7 KB (30654 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:fb35725bea18f664a5bb875f3b74b31ef0f6b7d9c1da80d373f3849e17c32ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144184619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9016a3e85c16ad01abaf55fd78f1ce45e0b784054ccad76b949de0dfdd30a6da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 30 May 2024 13:35:33 GMT
ADD file:8b016c2ebd388f0eef3c74518d8a51d2d0f91f909a2c8dc0cf8e895d6a603e0d in / 
# Thu, 30 May 2024 13:35:34 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 30 May 2024 13:35:34 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 30 May 2024 13:35:34 GMT
ADD multi:10a5b9e3ab6a191968d4e9508eca8f1cb30ca8c8ff6681dd9ecbea964c42b6de in /etc/yum.repos.d/ 
# Thu, 30 May 2024 13:35:34 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 May 2024 13:35:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 30 May 2024 13:35:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 May 2024 13:35:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 May 2024 13:35:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 May 2024 13:35:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 May 2024 13:35:34 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 May 2024 13:35:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 May 2024 13:35:34 GMT
ENV container oci
# Thu, 30 May 2024 13:35:34 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 13:35:34 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 13:35:36 GMT
RUN rm -rf /var/log/*
# Thu, 30 May 2024 13:35:36 GMT
ADD file:7a4eab654b9ca109b4f2363c082defccf7202d379a2669fd35283e0b49c8f37d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1717074713.json 
# Thu, 30 May 2024 13:35:36 GMT
ADD file:71d4936b52982664ba7256d377f39f0b718aa884683e99d20ecab908615c7df4 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1717074713 
# Thu, 30 May 2024 13:35:36 GMT
LABEL "release"="949.1717074713" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-30T13:14:08" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1717074713"
# Thu, 30 May 2024 13:35:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3133872-373bc.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 30 May 2024 13:35:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 30 May 2024 13:35:40 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 30 May 2024 23:03:04 GMT
RUN groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 # buildkit
# Thu, 30 May 2024 23:03:04 GMT
ENV GOSU_VERSION=1.17
# Thu, 30 May 2024 23:03:04 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.4.2 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 30 May 2024 23:03:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 30 May 2024 23:03:04 GMT
ARG MARIADB_VERSION=11.4.2
# Thu, 30 May 2024 23:03:04 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN set -eux ; 	curl --fail https://pagure.io/fedora-web/websites/raw/master/f/sites/getfedora.org/static/keys/FF8AD1344597106ECE813B918A3872BF3228467C.txt --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://supplychain.mariadb.com/MariaDB-Server-GPG-KEY --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-11.4.2 MariaDB-server-11.4.2 ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-11.4.2/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 30 May 2024 23:03:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 May 2024 23:03:04 GMT
# ARGS: MARIADB_VERSION=11.4.2
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 30 May 2024 23:03:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 May 2024 23:03:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 May 2024 23:03:04 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 30 May 2024 23:03:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:1380853393b36312aac70ccb4466a637b994f6a098d82d62044bfaf89ed2364e`  
		Last Modified: Thu, 06 Jun 2024 18:11:53 GMT  
		Size: 37.1 MB (37121384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eba5b94d24d5f747a6f809089f272d7a6eb6d16ed0472943d949ece34c18d9`  
		Last Modified: Fri, 07 Jun 2024 03:42:02 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7c788aaf83687ea49320ec8efaa74f11868acd6e64986117b79af1049288b7`  
		Last Modified: Fri, 07 Jun 2024 03:42:02 GMT  
		Size: 948.1 KB (948122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aba1f81058e608d5c0a081d503cf723c2b41b7279bd65f67cef6a813210ea8a`  
		Last Modified: Fri, 07 Jun 2024 03:42:02 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7a6f0c3601c61d34ee639f854ac87d56e742809fe112db5de66dc9b44a1a6b`  
		Last Modified: Fri, 07 Jun 2024 03:43:39 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a874e6d54dcc5df5308771655cf7548064ece6091b91ed1ddf3833cd7fbb18`  
		Last Modified: Fri, 07 Jun 2024 03:43:42 GMT  
		Size: 106.1 MB (106101556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cbf21b725e1ed4edffa01e6eb9dbdf145127d3518a546e283bcfa00086936d`  
		Last Modified: Fri, 07 Jun 2024 03:43:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2046758ff3f4e0e9935f27bf0139f128fa6caee3917b3afe275b904c3c4abaeb`  
		Last Modified: Fri, 07 Jun 2024 03:43:40 GMT  
		Size: 3.6 KB (3617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15428b1a3be1267c1c50932b74ea4d3c847cfd8ebb0251fbec3d94d50966c9fa`  
		Last Modified: Fri, 07 Jun 2024 03:43:40 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:1aa2632dafa2608c8386a48d1b2a6d06d09f55f832254378b1ab1374ec9a9867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bebec5cc6a0d10ee1bd9c4586236ab4e8d7e9df4558492f4e74b1e1551a2d9b`

```dockerfile
```

-	Layers:
	-	`sha256:4c96cb008964ef7d9c0d162fd0d6f0301490834eda7f2c289362b242b959ec7c`  
		Last Modified: Fri, 07 Jun 2024 03:43:39 GMT  
		Size: 3.9 MB (3885635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76dfda11592cbf4e35ffb7b37a021e2c2e5ba95668057b92e426faee237c0367`  
		Last Modified: Fri, 07 Jun 2024 03:43:39 GMT  
		Size: 30.6 KB (30585 bytes)  
		MIME: application/vnd.in-toto+json
