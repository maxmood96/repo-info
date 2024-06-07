## `mariadb:lts-ubi9`

```console
$ docker pull mariadb@sha256:5994bcc4ee014f3e39a662e6e04c942b5cbd344b11caed484104b6453e4afdf2
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

### `mariadb:lts-ubi9` - linux; amd64

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

### `mariadb:lts-ubi9` - unknown; unknown

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

### `mariadb:lts-ubi9` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:470b6a68ce916d247ec138c85f84d8ca999c23bf05e2219980cc84163c0845a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142054017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9f418e65818057b70ec2d7ed4bfc08a4a5dca3346c3ffbcb355ba0f0d71bf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 23 May 2024 13:57:51 GMT
ADD file:32aa20e449b3486807d09d4c296901fcc11bd3ac0350736dd920d37dabf414d7 in / 
# Thu, 23 May 2024 13:57:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 13:57:53 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 13:57:53 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
# Thu, 23 May 2024 13:57:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 13:57:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 13:57:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 13:57:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 13:57:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 13:57:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 13:57:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 13:57:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 13:57:53 GMT
ENV container oci
# Thu, 23 May 2024 13:57:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:57:53 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 13:57:54 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 13:57:55 GMT
ADD file:52288ae6de2702c2325e6cc064a56303f60253b9695a25411e571ba09df18eaa in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 13:57:55 GMT
ADD file:7a01c517d9beace4ea2a507407c840ca8ccd93e24a89ab5d836f247a9bd2ae0a in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 13:57:55 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 13:57:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 23 May 2024 13:57:58 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 13:58:00 GMT
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
	-	`sha256:03e931dae087208f4604cf960cff372993a4a6c742b5dd267e17106fa743d48f`  
		Last Modified: Tue, 28 May 2024 15:00:01 GMT  
		Size: 37.1 MB (37080662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dfdac00e769e950604a81b0f751c17aaa5fc4637d642c51efa48e99db65cf5`  
		Last Modified: Fri, 31 May 2024 16:21:56 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e3c1ec972143e05e54820b316e72e67d95605bca8e3b4109bf78323a747da`  
		Last Modified: Fri, 31 May 2024 16:21:57 GMT  
		Size: 913.8 KB (913801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f1baa3db0fce0445e6229de643fae9a1e5d2c087507c7937b63ad8e19c29a`  
		Last Modified: Fri, 31 May 2024 16:21:56 GMT  
		Size: 283.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9def812d59012b8f9992b20430771de1aafb961629173ca6b985bf84e914f63b`  
		Last Modified: Fri, 31 May 2024 16:26:02 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de97e1e95182184cdf291c79b5d002178afc0e9af9934ab674f80e017b9d68`  
		Last Modified: Fri, 31 May 2024 16:26:06 GMT  
		Size: 104.0 MB (104045999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d530ffbcfe666936b5bb9db6954c3ff3077ece56fa2ddc2da936c380bbf23445`  
		Last Modified: Fri, 31 May 2024 16:26:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addca78456279fa875aeeb2ec79edeb14069f165651c37d7449e125f0f7f7f4b`  
		Last Modified: Fri, 31 May 2024 16:26:03 GMT  
		Size: 3.6 KB (3618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a3c36c6b366b2f31b17d4e27fc4c4f7b55c1dadb45496334c750d5fc1c94fb`  
		Last Modified: Fri, 31 May 2024 16:26:04 GMT  
		Size: 8.3 KB (8343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:b6f8e4512d4d82bc6207bde23b4409552a982c6e2d7a877098c9a2280cddf457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c134b35d776ec51acfd81be24a3c619548f8dd3b91555ad440318c1c38ae83`

```dockerfile
```

-	Layers:
	-	`sha256:861eeafcd2afde01d40955eebd2efce2a2efe629f488a0cb875a8136ee366aff`  
		Last Modified: Fri, 31 May 2024 16:26:03 GMT  
		Size: 3.9 MB (3884469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f251cd24e18bf39aba163f1c3b0f316d652beed6e78b5b4f2b4f276f02d1212e`  
		Last Modified: Fri, 31 May 2024 16:26:03 GMT  
		Size: 30.9 KB (30892 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; ppc64le

```console
$ docker pull mariadb@sha256:85f5dedb1bbef34e276636eb2057f1e5c2939cd885565e3a77cc83bc17872f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156044500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d842d4ad96857ae1364da9defd5042937172e3722972ac0216fdc34ea09fc38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 23 May 2024 13:57:55 GMT
ADD file:0a163e5cc623159d8a10c082754e05de157bdde7729978401f1dad5f9701b130 in / 
# Thu, 23 May 2024 13:57:56 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 13:57:56 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 13:57:57 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
# Thu, 23 May 2024 13:57:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 13:57:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 13:57:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 13:57:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 13:57:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 13:57:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 13:57:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 13:57:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 13:57:57 GMT
ENV container oci
# Thu, 23 May 2024 13:57:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:57:57 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 13:57:58 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 13:57:59 GMT
ADD file:59d7a0456128ae89ea16e93b99c6691a9a59afb50f5392bf4ba22029f53d05a0 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 13:57:59 GMT
ADD file:3461432594d7ff6aade7d9ba0528b0105a1836fd26566a2271f6ce5bcc2c16fd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 13:57:59 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 13:58:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 23 May 2024 13:58:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 13:58:05 GMT
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
	-	`sha256:b5a9869bf68d50132f0329a511d3472c8ce0b262cb85d0b9ba8d4fe5e504b8ed`  
		Last Modified: Wed, 29 May 2024 12:11:52 GMT  
		Size: 43.3 MB (43314906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c20ead0508b04c5cf2ecba9efdeea23d2cf6cb35cf02e374c27b7d9b37a07e`  
		Last Modified: Fri, 31 May 2024 01:28:58 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b6f95d4f92addede3d32826a5d89a0fa0835123b2bc37193bb7715140654c2`  
		Last Modified: Fri, 31 May 2024 01:28:58 GMT  
		Size: 904.3 KB (904302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0151bb57411b39d980b8a71b7c8b36e5f7b9acd1c73f360a80085a016b4a1bc7`  
		Last Modified: Fri, 31 May 2024 01:28:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701c5be9e82d2ec4c632ddb6ab57f0f49df7c7616576aa9f78db49b471895c21`  
		Last Modified: Fri, 31 May 2024 01:33:50 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f753b09879983350b4e8bf228354290fe3248d27c05d45c8ffe4a79dc9f7d`  
		Last Modified: Fri, 31 May 2024 01:33:53 GMT  
		Size: 111.8 MB (111811739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62c2ae90a78ccffa62c61c859184a7db24e363a70f79a7b767f738e9eb19e26`  
		Last Modified: Fri, 31 May 2024 01:33:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea50250c176e1ae6465348bd3cdde82985d9d7f005602cb944f7b4f6c16b7236`  
		Last Modified: Fri, 31 May 2024 01:33:49 GMT  
		Size: 3.6 KB (3615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3134620323b3438ddc2740dc6bad1490df163b0bc065fb72ab9c4f4f372720d8`  
		Last Modified: Fri, 31 May 2024 01:33:50 GMT  
		Size: 8.3 KB (8339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:4ac9d85d3c9ad7ebf4601961c7fa2f4b8cba9341a221237df5f1d1676891e126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f09bb12db92797fa99046a896964406d1ac441ff362f700058d0e0112ae5e14`

```dockerfile
```

-	Layers:
	-	`sha256:b78fbb68f5c0bbf968e29058207c4cffba874ac3e450816e43b37d000cd8611a`  
		Last Modified: Fri, 31 May 2024 01:33:49 GMT  
		Size: 3.9 MB (3885662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96220becf602e0d34b70f5a2d70179c75c49a1b26de79c6b22a55cc1a321f29`  
		Last Modified: Fri, 31 May 2024 01:33:49 GMT  
		Size: 30.6 KB (30605 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-ubi9` - linux; s390x

```console
$ docker pull mariadb@sha256:cb324b31929ed958a6c3cb2d73df27850e00986a8d2e828e254a26bf45b68064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144260868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ac3d4edb71c8844cf21f5beaac7bcc6879fb1d7ccaed6742762b4c4eb883c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 23 May 2024 13:58:06 GMT
ADD file:798b7a2209629e07af18955422fac24bc8e70bab90cc0d26a8b853277bd2644f in / 
# Thu, 23 May 2024 13:58:09 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 13:58:10 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 13:58:11 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
# Thu, 23 May 2024 13:58:11 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 13:58:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 13:58:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 13:58:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 13:58:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 13:58:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 13:58:11 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 13:58:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 13:58:11 GMT
ENV container oci
# Thu, 23 May 2024 13:58:11 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:58:11 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 13:58:14 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 13:58:15 GMT
ADD file:750c52518541df4f4a6417171fb56dcf4f4073f467939d0505590148498ae4b3 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 13:58:16 GMT
ADD file:87fe2066c3b36663dc4ed1d2b7f3039618e482f655f701d6035dbf482e5b57a3 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 13:58:16 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 13:58:19 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 23 May 2024 13:58:22 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 13:58:24 GMT
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
	-	`sha256:258e30c6f516fe7233d638e11a594714dfe8e78952d8eecf1f69907c371494df`  
		Last Modified: Wed, 29 May 2024 12:11:58 GMT  
		Size: 37.1 MB (37121987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e00e7844205266f9ef95b2e74ed00118effab8f9bcbc5877a9ff20392fe308`  
		Last Modified: Fri, 31 May 2024 02:18:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2d2f0c2a2a2af9a1e5b3253ce706646284dfda60b7fe44192c9de73eb7847a`  
		Last Modified: Fri, 31 May 2024 02:18:01 GMT  
		Size: 948.1 KB (948121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d610e495784b0a4866ecf436b7ce68ea56337c743e00007c79ff00b6473df1b`  
		Last Modified: Fri, 31 May 2024 02:18:01 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a6b984a15ee329070e17dc8c82f4d25ac0928166b9a2a2fbd5c615e18b0af9`  
		Last Modified: Fri, 31 May 2024 02:21:05 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9af33ac26cf512eeece9475f26058824278c65d790e1883f7311b9aa26da971`  
		Last Modified: Fri, 31 May 2024 02:21:09 GMT  
		Size: 106.2 MB (106177212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eed2c1158e0d7bd7f7bd8746408e6439e5dd039ff982ade7054168cb0d495d0`  
		Last Modified: Fri, 31 May 2024 02:21:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c28e7fd3dc76eada6e404b58c3dc880745ca7d46baa0c8c55a5a8702aedddb9`  
		Last Modified: Fri, 31 May 2024 02:21:05 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca015f450af329b245bf5146a8950bb59ba6f926e9693ecdbd1312ce0c55e94`  
		Last Modified: Fri, 31 May 2024 02:21:06 GMT  
		Size: 8.3 KB (8339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:bdd77bda4ed9454d66c6335203c829946216888118fd1dc65f1769976199d447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3916172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc11023c81f322def076a1f7cacd4c674f8c841f9c84f88ae1242b3c386dbee`

```dockerfile
```

-	Layers:
	-	`sha256:3ca94992b72bdbdfd5a623f205e5dcd060a32c800d9b354d6f2dc7469b0ca4a2`  
		Last Modified: Fri, 31 May 2024 02:21:05 GMT  
		Size: 3.9 MB (3885635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95baf7b36131251403e71bc53225598aa1d0c939daee54bdc6c648830c23ff1f`  
		Last Modified: Fri, 31 May 2024 02:21:05 GMT  
		Size: 30.5 KB (30537 bytes)  
		MIME: application/vnd.in-toto+json
