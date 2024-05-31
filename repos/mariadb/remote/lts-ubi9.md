## `mariadb:lts-ubi9`

```console
$ docker pull mariadb@sha256:f8b2b95538f0cc5a835bf23dbd5681f92955413295675d74a1d45c0bedd564bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `mariadb:lts-ubi9` - linux; amd64

```console
$ docker pull mariadb@sha256:600bd927bc1727d8ccb695cb27935324380fc65adc8d7ab1022a95f3b4e824c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145540202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b57ed67c71aa6aeda873403c69365a1636725a8dc7f26a4320d13a1a705a7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 23 May 2024 13:57:54 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 13:57:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 13:57:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 13:57:56 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
# Thu, 23 May 2024 13:57:56 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 13:57:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 13:57:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 13:57:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 13:57:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 13:57:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 13:57:56 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 13:57:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 13:57:56 GMT
ENV container oci
# Thu, 23 May 2024 13:57:56 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:57:56 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 13:57:56 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 13:57:57 GMT
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 13:57:57 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 13:57:57 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 13:57:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 23 May 2024 13:57:58 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 13:57:59 GMT
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2f07caf93b3f108a5d1b458c2a5557bf6a14a67326f4fadf7d9cec076dd2c2`  
		Last Modified: Fri, 31 May 2024 00:57:16 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9a932f9b9c056ba9ef7a58381cda2d08d1c28c465021782c689633626ebcae`  
		Last Modified: Fri, 31 May 2024 00:57:17 GMT  
		Size: 983.5 KB (983466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b051ac0d77fef1c27fe6d5e6df9984dc92018142b6399c0701715df61097a2d3`  
		Last Modified: Fri, 31 May 2024 00:57:16 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9758876b4afd70396cf72ef52d9ff1aabdf73aab2a1cf3f805f0962e016f660`  
		Last Modified: Fri, 31 May 2024 00:57:17 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500746a3f20fd0a31c06563736fadb80787c4bdf15471ac015d1f6c00e36cd4e`  
		Last Modified: Fri, 31 May 2024 00:57:19 GMT  
		Size: 105.7 MB (105666128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e60f66e2591267fae44257e522da196e6200a6d4642dc80918a6737f81bd83`  
		Last Modified: Fri, 31 May 2024 00:57:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803d3ff54cb9a26706e5c6c7e1978a8027b84369a0c22865a238d7d717c4cc65`  
		Last Modified: Fri, 31 May 2024 00:57:17 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f947e2e9eb6847513d470723fb4db2e8ffbe5e02b009d09ba1669861756bc887`  
		Last Modified: Fri, 31 May 2024 00:57:18 GMT  
		Size: 8.3 KB (8338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-ubi9` - unknown; unknown

```console
$ docker pull mariadb@sha256:3fdc6a4813acc8078da00ef244b497e70d5e1e17ada9e1af6d0bf4de70b3c345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d693a15ac692a8927579c1fb1c9b15b47ca430adc6024eff94372805df788768`

```dockerfile
```

-	Layers:
	-	`sha256:f2e20961d811218fa18cec6e7acd6c5db2df356e90cca1889039e91381c89056`  
		Last Modified: Fri, 31 May 2024 00:57:17 GMT  
		Size: 3.9 MB (3884637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b826e05d8bba741442a57786af89ca015428d4c9e006b9d9b46bc40a82705f8`  
		Last Modified: Fri, 31 May 2024 00:57:17 GMT  
		Size: 30.5 KB (30537 bytes)  
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
