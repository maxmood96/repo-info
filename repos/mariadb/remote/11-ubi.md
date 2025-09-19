## `mariadb:11-ubi`

```console
$ docker pull mariadb@sha256:ce99fbea8285caf0f45fff2a7534e779885d6d45f1c9f71161db0636cdd68558
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
$ docker pull mariadb@sha256:646694be69540827cec504ceda16f25220a1b0dd2f6b7bd6e043839782fe4efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155217904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7cc49182b554a61c58ec5507938dc4eed4ec2bf2dd0815236ad4161e9d40cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.expose-services=""
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 10 Aug 2025 22:04:52 GMT
ENV container oci
# Sun, 10 Aug 2025 22:04:52 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["/bin/bash"]
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Sun, 10 Aug 2025 22:04:52 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENV GOSU_VERSION=1.17
# Sun, 10 Aug 2025 22:04:52 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=11.8.3
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=11.8.3
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=11.8.3
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=11.8.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 22:04:52 GMT
USER mysql
# Sun, 10 Aug 2025 22:04:52 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4afce221d19117dd2752a4df07a200504c1f2c898de43c8117ee5f4aa15ed6`  
		Last Modified: Fri, 19 Sep 2025 20:46:02 GMT  
		Size: 4.8 KB (4771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22da05f4a736cef3996eca2fb315834490a5273cca937c868d28429c9b6cf5c`  
		Last Modified: Fri, 19 Sep 2025 20:46:02 GMT  
		Size: 2.0 MB (2001918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63084f920e18596143bb842ce22e661e10a9490ae27d11a48e08da0ffa8a0516`  
		Last Modified: Fri, 19 Sep 2025 20:46:03 GMT  
		Size: 7.0 MB (7041970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a36a90d529ebf67ce937ee87a686f15e1d5a4686b03e5cc617f6347956f3446`  
		Last Modified: Fri, 19 Sep 2025 20:46:02 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8282ccf7c3c6be232a4571dceea37220f7ddb42fb7d657793124331d825477ca`  
		Last Modified: Fri, 19 Sep 2025 20:46:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf4e2245d8e975d074c04fdb07df146e4b16cd615d06a7fab256b40541f389e`  
		Last Modified: Fri, 19 Sep 2025 20:46:10 GMT  
		Size: 106.5 MB (106507810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4652ca963d59f11d0365e1cfc0395be1a4a332fd976e0c436a5d5328a5bb7788`  
		Last Modified: Fri, 19 Sep 2025 20:46:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b5c6312bd83e833bebc769161681d64a9407e4c32de4bd96afce825cbe3564`  
		Last Modified: Fri, 19 Sep 2025 20:46:02 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaf7fe927571c0991e87d17d998c442b1d793c9f9d86f9ba6c2f1e05ea995da`  
		Last Modified: Fri, 19 Sep 2025 20:46:02 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:5b840650e69a1ffe1f5ef2c5d9aaec5cf061f28704ba62854eb2014dad46fc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4159981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd8ac3e5a32933d94e72a06301da9def70e0a5f1bb17cabd16e736e4ddcbc53`

```dockerfile
```

-	Layers:
	-	`sha256:260d9ebd503f0bbd26b7e2663986d0cda8900153b8d3da8108dc02fc61e9874d`  
		Last Modified: Fri, 19 Sep 2025 21:36:13 GMT  
		Size: 4.1 MB (4125639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f15af9f74a5ddd1f7a9f1ececed47afba2bb91eb22cdcde02ec82d6740fd5d`  
		Last Modified: Fri, 19 Sep 2025 21:36:14 GMT  
		Size: 34.3 KB (34342 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:85910ebc9c3032838356d8de003e3cc47554e3f991073371ce2834e1636ee3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151026074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e3301a728bf16b39ddc23ec372d196f7a012f15dfc071d3864408d0c1c1af4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.expose-services=""
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 10 Aug 2025 22:04:52 GMT
ENV container oci
# Sun, 10 Aug 2025 22:04:52 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["/bin/bash"]
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Sun, 10 Aug 2025 22:04:52 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENV GOSU_VERSION=1.17
# Sun, 10 Aug 2025 22:04:52 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=11.8.3
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=11.8.3
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=11.8.3
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=11.8.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 22:04:52 GMT
USER mysql
# Sun, 10 Aug 2025 22:04:52 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786693ae8364a16735861b3450dc3eb7b9546ee0f24e29e2cb8874a1b9cb0fe3`  
		Last Modified: Fri, 19 Sep 2025 20:45:51 GMT  
		Size: 4.8 KB (4771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3323df028364f3f6626a6ed789b80cc05a13e9b2aaa500fe521201fcb071727`  
		Last Modified: Fri, 19 Sep 2025 20:45:51 GMT  
		Size: 2.0 MB (1996757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5111de8ccef2c640ce54e02decdb0c6c5c7eb946945d1cbe0f0ca3a6376ce1aa`  
		Last Modified: Fri, 19 Sep 2025 20:45:52 GMT  
		Size: 6.1 MB (6098129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf0e8c23e50e14921da3adab052930c201959210aa9ca582e4f3666821ee385`  
		Last Modified: Fri, 19 Sep 2025 20:45:51 GMT  
		Size: 301.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd98ccf9f42b71df51600ff3a8aff4dc073c0a3f334db22d6d3901c039591ff`  
		Last Modified: Fri, 19 Sep 2025 20:45:51 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d49a198cb70370aa7e0b73e01f8afbdbf5322bc011846dfea1f048ab985ebaa`  
		Last Modified: Fri, 19 Sep 2025 20:45:56 GMT  
		Size: 105.0 MB (105013078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f71bf5c19467173ea6c55e45a35565d1c039cb1e798aea5560298be88cbd0e`  
		Last Modified: Fri, 19 Sep 2025 20:45:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607a47b04b0b0de5129d22f3fd68b269c419c5e34606784678ed28d0130b3378`  
		Last Modified: Fri, 19 Sep 2025 20:45:51 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58014e21d585472bcc300939662a81b211671dde45173693c0c6f4ebdf4037c`  
		Last Modified: Fri, 19 Sep 2025 20:45:51 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:6a3b4da1e68d80e759a4b96742b764de405361108a7d312e4d05a862e02f5893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4160253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb60a58874e5cff701106b06ea9abd4f7b54e6ae05412b40cc194ecb836a6fa`

```dockerfile
```

-	Layers:
	-	`sha256:460e7a880c5c843527d0aec7130568061f257ac7cbf46defbc9a6660a1d06041`  
		Last Modified: Fri, 19 Sep 2025 21:36:19 GMT  
		Size: 4.1 MB (4125705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c5f49cff7e695844e772e1d5818f7d5b1e86cd43aee1a3ebe115f33fb6a09e`  
		Last Modified: Fri, 19 Sep 2025 21:36:20 GMT  
		Size: 34.5 KB (34548 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8d3c2c40c6c717e6019d8c5707b9e8174024bb197002c6450efa58e5942e1d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164966652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8098e9675b074b09471a16da0e803eedc1cf3be87c01395c29ad5414a11705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.expose-services=""
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 10 Aug 2025 22:04:52 GMT
ENV container oci
# Sun, 10 Aug 2025 22:04:52 GMT
COPY dir:d2207f84596636cf1f42082a4111b6c38656ec970ae8b2e1ce2cacd7d29f1510 in / 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["/bin/bash"]
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL "build-date"="2025-08-20T13:11:42" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Sun, 10 Aug 2025 22:04:52 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENV GOSU_VERSION=1.17
# Sun, 10 Aug 2025 22:04:52 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=11.8.3
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=11.8.3
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=11.8.3
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=11.8.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 22:04:52 GMT
USER mysql
# Sun, 10 Aug 2025 22:04:52 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:ebd7c9ee3cc0108f33ad80f84c3da96a78c10cc76b3dfe38b2b8ab879a83a307`  
		Last Modified: Wed, 20 Aug 2025 18:13:19 GMT  
		Size: 44.1 MB (44057494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ab0339a62212469391e8fcb5883cf9c96859b56f720a650a8278286b5a2bca`  
		Last Modified: Thu, 21 Aug 2025 19:22:46 GMT  
		Size: 4.8 KB (4770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3578090037abd18b7884160fc2c7e48225b3bad9d39c4a79cad38d5c76e26746`  
		Last Modified: Thu, 21 Aug 2025 19:22:47 GMT  
		Size: 2.0 MB (1994155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377b2324eca093eb84fbb4c1bad2daaf206c86fcb6f04e92592ff311189a15c9`  
		Last Modified: Thu, 21 Aug 2025 19:22:47 GMT  
		Size: 6.1 MB (6069585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025696d3557ad2a4c11a5a75db6343e502737f889647326fe0a3c30602902a71`  
		Last Modified: Thu, 21 Aug 2025 19:22:47 GMT  
		Size: 299.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c739c3ecbe2e110e311f7e5878d4e247c506b7c0f12995e37918ad467d0f6f0f`  
		Last Modified: Thu, 21 Aug 2025 19:22:47 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d568b305028bb24c6d111fa83b6775893d5f11e953865a99f495beaa163eb45`  
		Last Modified: Thu, 21 Aug 2025 19:23:13 GMT  
		Size: 112.8 MB (112827468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f27fdf83f09c2e199117db93524ca939ff1e8710f61d3eb46101e94e1b9a99`  
		Last Modified: Thu, 21 Aug 2025 19:22:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863eceb82193c70d979d01c8efd84b0b73dce2a0211d25607016968619d24578`  
		Last Modified: Thu, 21 Aug 2025 19:22:48 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498b5ebb1e6be37821bbcf8d513a91546e1ed85fc5e28524542f3ff2f7f72992`  
		Last Modified: Thu, 21 Aug 2025 19:22:48 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:c68c469537dca5b6b6c7dd89af957ea0bd2d51837eb72b076726ce1b9ad2c214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4161300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05bca0f406968358664487a9df32d999192410075052707bad13435a53408e4`

```dockerfile
```

-	Layers:
	-	`sha256:4a28f1d45c0e93b51beff48451ec4e3026086a5ec95a8be61f078374d9baa226`  
		Last Modified: Thu, 21 Aug 2025 21:37:09 GMT  
		Size: 4.1 MB (4126888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7e29c769a0cabbfe5f489b3b8d665ecf553b931dd7dfdd4b596edade040936`  
		Last Modified: Thu, 21 Aug 2025 21:37:10 GMT  
		Size: 34.4 KB (34412 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:721d5d85dddbb6950ed9a22ed7183b71a47b68e1daa02a9e2eee8ef706f6b5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153062798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53796bc856592863c9461ae99e54c5809e4b37ff24b7d08c3e98a1d4b52feefe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.expose-services=""
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 10 Aug 2025 22:04:52 GMT
ENV container oci
# Sun, 10 Aug 2025 22:04:52 GMT
COPY dir:50d215ebed2bd8f3ebc927c36f9221810f1ee237dd8666d613479d55333c24b0 in / 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["/bin/bash"]
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL "build-date"="2025-08-20T13:21:17" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Sun, 10 Aug 2025 22:04:52 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENV GOSU_VERSION=1.17
# Sun, 10 Aug 2025 22:04:52 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=11.8.3 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=11.8.3
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=11.8.3
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=11.8.3
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=11.8.3
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 Aug 2025 22:04:52 GMT
USER mysql
# Sun, 10 Aug 2025 22:04:52 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 10 Aug 2025 22:04:52 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3f0282e908208d8e7c1713535fd66f131da1a731129cef1ea3f76c45ef5710cb`  
		Last Modified: Wed, 20 Aug 2025 18:13:17 GMT  
		Size: 37.8 MB (37760918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7a7e68b5341da44b8c40fb1b75804c3182780d7a38870b1de1e994970ab7cd`  
		Last Modified: Thu, 21 Aug 2025 19:59:04 GMT  
		Size: 4.8 KB (4770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf999c0ae982281487553148ef65240526a638882c6f6b2418e59740e69e15f0`  
		Last Modified: Thu, 21 Aug 2025 19:59:04 GMT  
		Size: 2.0 MB (2010429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9919c9f469f391b773c2e69c4c19ff1a921976d3116d6cee333896727a49af20`  
		Last Modified: Thu, 21 Aug 2025 19:59:04 GMT  
		Size: 6.1 MB (6084937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feeb3d46b406a76c728d2c9c75af7d836d1c2cacefb0bbaea255d6e87c891037`  
		Last Modified: Thu, 21 Aug 2025 19:59:03 GMT  
		Size: 300.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d051c07565c9a6facdc0c93a12af995e2de3b65935dfc40c36b2db7664105d7`  
		Last Modified: Thu, 21 Aug 2025 19:59:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb12eef3d0690f6a666ab4c7d74befc25de60ad1316f512abe0a4ed04ea2cec`  
		Last Modified: Thu, 21 Aug 2025 19:59:14 GMT  
		Size: 107.2 MB (107188552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f587e539a8f71fa04bd1998db308d1a0e020e20e212243b6885152d12d63036`  
		Last Modified: Thu, 21 Aug 2025 19:59:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2628e66841b2f85cca035616aedd3f40a6b10f8ea1d2839e4db42437c3921e0b`  
		Last Modified: Thu, 21 Aug 2025 19:59:04 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6127cd6eb9737c9c1f042970b555a083f1de749aedd83e37895704621b61c649`  
		Last Modified: Thu, 21 Aug 2025 19:59:04 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:b55ca6eefe28a5286a1d42ed17f1306080f81373f1c9b11a22df6475acd448f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4161203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c939b87bef433658954873da2fc01eac125eaf22654fd9d9286157f9f3a138e2`

```dockerfile
```

-	Layers:
	-	`sha256:0ae6c3285b3a08b09f49c301fbd794214941a852dbae9ddb047f95dc6cf038c2`  
		Last Modified: Thu, 21 Aug 2025 21:37:15 GMT  
		Size: 4.1 MB (4126861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5fab1d8731ca4e50d3328d313411607a69107dc5d4ab6ebe223abdc1a2ec47`  
		Last Modified: Thu, 21 Aug 2025 21:37:16 GMT  
		Size: 34.3 KB (34342 bytes)  
		MIME: application/vnd.in-toto+json
