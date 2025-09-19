## `mariadb:10-ubi`

```console
$ docker pull mariadb@sha256:4aa24d34787f16f73bf9f43fed13836f551cb94d45ef1f27ea3362b72e263763
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

### `mariadb:10-ubi` - linux; amd64

```console
$ docker pull mariadb@sha256:42a4a86f2c3b84c4d56de47721641e4540ff49670587be6d77a494fd8a1a2a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154147969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cd9fb9b86fc9b2506d0d8a0419881e71bab524603f07b67565e319142ee274`
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
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.14 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
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
	-	`sha256:ac8fc7c0aa4d85b778515820fdea86b60f43717c84ecd8e956d4deb908c57383`  
		Last Modified: Fri, 19 Sep 2025 20:46:02 GMT  
		Size: 2.0 MB (2001910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb021f321552e46291e36c34532dc3805ae63c715c9fa855427795ce59fbc12`  
		Last Modified: Fri, 19 Sep 2025 20:46:02 GMT  
		Size: 7.0 MB (7041965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042b8427b50b2d094a9252ba69220c809cdca643dcc76bc9bf2158dfdcc46ca7`  
		Last Modified: Fri, 19 Sep 2025 20:46:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70461c237140d024661d4b6f01b2a3f1a4c1ac42681c3a2204c354a8e8e4fb73`  
		Last Modified: Fri, 19 Sep 2025 20:46:53 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dce497cee6af7f2db9bbda6d8ddc6ccf94605177d63896c78d4d246dc4d45db`  
		Last Modified: Fri, 19 Sep 2025 20:47:00 GMT  
		Size: 105.4 MB (105437914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4e891277c2c58dabdc502fbd7bae3cda39ef371884ec788a6190a20c06005a`  
		Last Modified: Fri, 19 Sep 2025 20:46:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769e7abee2ff51d755b08441b91e43c393f44b39678e28d381af72f1bee4ae71`  
		Last Modified: Fri, 19 Sep 2025 20:46:54 GMT  
		Size: 4.0 KB (4017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bd50ccdb4f11f425b7ac21b82fcafe021366dc6289270ccbec5600a6663fe6`  
		Last Modified: Fri, 19 Sep 2025 20:46:55 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:dbd5083753314630a15336d9c29650e2d8d20c2944e10c6eb145dd8a1269fedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2012a3b65f3ddca01f2a8a6e2f54c49023e7d27bcbfa5d3de6b19efa9ef2c5`

```dockerfile
```

-	Layers:
	-	`sha256:5f21f3bc216a2ffc6b0b8a1c708cb2504093e81265e63cb7d79d9829bc0d5cef`  
		Last Modified: Fri, 19 Sep 2025 21:35:26 GMT  
		Size: 4.1 MB (4118240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e9c8d0246a303785a94083b68cbb4ed70cee915e5631b738ee787544abe72a`  
		Last Modified: Fri, 19 Sep 2025 21:35:27 GMT  
		Size: 33.8 KB (33763 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c02e1d97b7f2e4064050a0ec1a13e5016469b57cdc612f9e5909beb17940bd8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149862489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c567b914d6edb7f3c349d5d8334e7f38dd3d7f89cfa26574ba93928c377610b`
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
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.14 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
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
	-	`sha256:02f94f81e5a953e32bbc343bbea1c87cbd1d83f0c26a7d00df3b887a19cf1c43`  
		Last Modified: Fri, 19 Sep 2025 20:45:53 GMT  
		Size: 4.8 KB (4772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178d94be454fda5b59e2ae7310efe5ef0ae4fc4b307a8c06d108a8eb723e6edb`  
		Last Modified: Fri, 19 Sep 2025 20:45:53 GMT  
		Size: 2.0 MB (1996746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75384b96abb39914181d75c1b0c465d7b026fcb3c9d5051ebd14ce6ba719f5e2`  
		Last Modified: Fri, 19 Sep 2025 20:45:55 GMT  
		Size: 6.1 MB (6098130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae064db4cbcf8396963575bee20843b0de6cf9a24171162deca86ee97291a101`  
		Last Modified: Fri, 19 Sep 2025 20:45:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c812ff2cb5ed8326064e54ae562ea128516a9f61d3fb74699b3ce7d2bfc7a3b2`  
		Last Modified: Fri, 19 Sep 2025 20:45:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5e9f56cb8a48c29a97b8d4413582489b17a56110ff77d49122411852615c4c`  
		Last Modified: Fri, 19 Sep 2025 21:16:39 GMT  
		Size: 103.8 MB (103849520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d7b9d8eed475872d8b7ee57bb997e6ca1e2d5c87b417e4c31adf16cb868f7c`  
		Last Modified: Fri, 19 Sep 2025 20:45:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61fa77bf1d23e8887e55de6dc257e91941c9d4ced330667c6aaacea4ee93520`  
		Last Modified: Fri, 19 Sep 2025 20:45:55 GMT  
		Size: 4.0 KB (4017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8827912fb4005e0bd3b5e9f1fac75dfe495242f59f373d47f3f3b3dee6005de0`  
		Last Modified: Fri, 19 Sep 2025 20:45:56 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:43cbec1e2a74cc15492596de26c801b9e92496c5db4eaf92c24bf63125c62262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36edbe61f7c6b434b5b6103fc80fbd0b4580ebac606bb2decc3e14a2c1ad7e9a`

```dockerfile
```

-	Layers:
	-	`sha256:6dc5e453b6af8d09bd63863f2b2b706fb4fc5cfc11865c15f488f33fe4b8e1e7`  
		Last Modified: Fri, 19 Sep 2025 21:35:32 GMT  
		Size: 4.1 MB (4118282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed0cee43e8d0321012d397ac312c529bbca3d310c53fe9b6e772e91b7f58e2a`  
		Last Modified: Fri, 19 Sep 2025 21:35:33 GMT  
		Size: 33.9 KB (33944 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:91c29d0628797a08154d0b18de6730ab8188b7bbedc2fc2b3e4ca45b384c0b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163676166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8550b5e211dbad027b536168fee095dc376108ba20e4048861149b7e69da9da`
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
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.14 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
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
	-	`sha256:2dc90396eb740846c9eb7121c6d8f9e084397169303b581b96455f9354fe9bba`  
		Last Modified: Thu, 21 Aug 2025 19:26:09 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2eda08479e6fe3e27fbeaa0bdaec3ac09a6905fe7fdc625aa391c95035227`  
		Last Modified: Thu, 21 Aug 2025 19:26:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ce913c059b1fed1d56c26b53ea2503730afe71f3f5d9cc7c43845571bec0cc`  
		Last Modified: Thu, 21 Aug 2025 19:26:22 GMT  
		Size: 111.5 MB (111536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54684b548a48e0073454be46f5eda01fe9873e3e20172638a7a36ad85bdd0f9`  
		Last Modified: Thu, 21 Aug 2025 19:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8142ee6f6354b523a90e4e76d678e5176403dcb3c2c6c9d10ba91db2671ce9c`  
		Last Modified: Thu, 21 Aug 2025 19:26:10 GMT  
		Size: 4.0 KB (4015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a501b6fe5c65c113e7d2403f34de6ec75a74af6b3778a4a909970c9c2d3bf76`  
		Last Modified: Thu, 21 Aug 2025 19:26:12 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:d3850a5e789fedde65a39939b9b14defe011487d59f608afbfbed2692a6c4a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4155982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfe837c2697fb2f196521257fd4beda5ed13d5d085e10c27d3a90f8ac1cfe75`

```dockerfile
```

-	Layers:
	-	`sha256:bd85e95388365ea5b2bd3aea63431e4792351102b2a331204365aa7d58dcc178`  
		Last Modified: Thu, 21 Aug 2025 21:35:44 GMT  
		Size: 4.1 MB (4122161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090a8bb3a8abb9b756d87d94f6f214c5d4de30d1a074f4a0b48330ccc9df89d0`  
		Last Modified: Thu, 21 Aug 2025 21:35:45 GMT  
		Size: 33.8 KB (33821 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:14b1152ee5ac3dbfac15729d0d12caefd801f62b3a6e9c4088d8900afc76c742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151933292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499d36ecc7df3c13521ada0ab5aff22ca3e8d533a732c94ac4e7051bcf10480e`
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
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.14 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Sun, 10 Aug 2025 22:04:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 10 Aug 2025 22:04:52 GMT
ARG MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
ENV MARIADB_VERSION=10.11.14
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Sun, 10 Aug 2025 22:04:52 GMT
VOLUME [/var/lib/mysql]
# Sun, 10 Aug 2025 22:04:52 GMT
# ARGS: MARIADB_VERSION=10.11.14
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
	-	`sha256:df07d9e360890b641fea26d52eeabb31229178218fe329efd253c106bf344238`  
		Last Modified: Thu, 21 Aug 2025 20:07:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e86dec9fcc4a5f230b5ec32efdd7ff42c06388587ecbd63e0731938ee3334`  
		Last Modified: Thu, 21 Aug 2025 20:07:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831e525c380ec60beb83451adeb717bf597f6fd2a58cdfe10a1ce9b4939ea63b`  
		Last Modified: Thu, 21 Aug 2025 20:07:18 GMT  
		Size: 106.1 MB (106059060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6396ead516f47ac98a2051e754e7caa45779f085c6fc1afb7e6ad5a0e92a54e7`  
		Last Modified: Thu, 21 Aug 2025 20:07:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7f81b47c3c8848702261792c31d218df2354853ef8c9cae7c4f68586ac4441`  
		Last Modified: Thu, 21 Aug 2025 20:07:05 GMT  
		Size: 4.0 KB (4020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9d7f082f5e84887bbe0e4180c7d8a6232278ab380075a8756d0715ba46c2b4`  
		Last Modified: Thu, 21 Aug 2025 20:07:05 GMT  
		Size: 8.4 KB (8368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:2595f532956d94b6891b04ddf4a89d6ac4fa2555a6f068012ff1f341e5b61669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4155909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6337b14c1d41953aaba7d6bc0c1abe4ee5416cc830106501add71ba3f55212`

```dockerfile
```

-	Layers:
	-	`sha256:29eab4442c4d609e28a3b88355744ba7505459cdebc9715a78b372a72b9fdcb2`  
		Last Modified: Thu, 21 Aug 2025 21:35:50 GMT  
		Size: 4.1 MB (4122146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c41c502376f8ef1f53799937aeae8b990438a1fd5d3ec72ab97fdcd1c58191a4`  
		Last Modified: Thu, 21 Aug 2025 21:35:51 GMT  
		Size: 33.8 KB (33763 bytes)  
		MIME: application/vnd.in-toto+json
