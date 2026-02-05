## `mariadb:10-ubi`

```console
$ docker pull mariadb@sha256:1a3dba61b4ba31fff0969feda54fa96f47456efc36660106a5284509d62c5f54
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
$ docker pull mariadb@sha256:8a16661bb28c123e1949c5e5f956f470aebc2ce00b1bb564d6d138761fbc1e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166519187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c30f79fa634a0a79cba96b4f8c16d2eca866b5653ce282dfbb3ffa1386568c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:16:43 GMT
ENV container oci
# Wed, 04 Feb 2026 11:16:43 GMT
COPY dir:e45f16623580cdab20a9c9f5e40207717eeb9bb3de78238f58a6f3e3c0582b7c in /      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:16:44 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:16:28Z" "org.opencontainers.image.created"="2026-02-04T11:16:28Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:16:28Z
# Thu, 05 Feb 2026 00:10:45 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 00:10:46 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:10:49 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 00:10:49 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 00:10:49 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 00:10:50 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 00:10:50 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.15 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 00:10:50 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.15 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 00:10:50 GMT
ARG MARIADB_VERSION=10.11.15
# Thu, 05 Feb 2026 00:10:50 GMT
ENV MARIADB_VERSION=10.11.15
# Thu, 05 Feb 2026 00:11:12 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 00:11:12 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 00:11:12 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 00:11:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 00:11:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:11:12 GMT
USER mysql
# Thu, 05 Feb 2026 00:11:12 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 00:11:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89e9253af18d5c0ff4d09a59691ba4c31a249cfb098777551798316abee90a5`  
		Last Modified: Thu, 05 Feb 2026 00:11:32 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667c4868e3b3dc7d1be661e37c5e10918a86e6ef2cfd80d1e6d1815b3c537e73`  
		Last Modified: Thu, 05 Feb 2026 00:11:32 GMT  
		Size: 2.0 MB (2006755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b997b8cb996974ddde37ed65f8b09802f57d8cebafdd25f26362fa76cfba09`  
		Last Modified: Thu, 05 Feb 2026 00:11:32 GMT  
		Size: 7.2 MB (7202525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a40ab2b092f1c818d138f50e919aa1ec0ae8400157012af71ed828fdf430ab`  
		Last Modified: Thu, 05 Feb 2026 00:11:32 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb68932a53fb25436ddd4eff5bbbb8570816ed27b86a119df978a006b14fcd4`  
		Last Modified: Thu, 05 Feb 2026 00:11:33 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c536e06ce5ef6a5b577041af26ab38562e5e94f9c140e077a06056013ee1305a`  
		Last Modified: Thu, 05 Feb 2026 00:11:36 GMT  
		Size: 117.3 MB (117282925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23748c6fc5297b9f5cbaae704cf9b2d06036b350032c769856d3ba1247a8d7b`  
		Last Modified: Thu, 05 Feb 2026 00:11:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701fe2e0d4bc439ed709c9622e52355e9a181abf6dbb7415208cb660ddc9cd03`  
		Last Modified: Thu, 05 Feb 2026 00:11:34 GMT  
		Size: 4.0 KB (4015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ae204400a89985b00ccbf38c9708ea4a4a999de927dd8164d242bae7849bb5`  
		Last Modified: Thu, 05 Feb 2026 00:11:35 GMT  
		Size: 8.4 KB (8361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:9bd7924f293ca873a49b589d39cdc74ee55a00a2a0b77f9c02cd2631077542fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec98a079132c49eb21c556d29dfb8fe4d9ca1a5171e85cc257939c1448f8fe5d`

```dockerfile
```

-	Layers:
	-	`sha256:b46b4ddc6ee24256ae416778df29a4d8fd89d6829940589c7e79b5fb48e84cc3`  
		Last Modified: Thu, 05 Feb 2026 00:11:32 GMT  
		Size: 4.7 MB (4726097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b7aa48802d741f1a6500816195a7b89c028446cb7f732a364277ef7c650a35`  
		Last Modified: Thu, 05 Feb 2026 00:11:32 GMT  
		Size: 33.8 KB (33848 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:7efd4604eb62bfc18c25ebb170208358b0b20f8e301f386ee13ee42a5d9dce11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161785062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0137dd2201058b1ed80576e990f76efd0bff351df336b968d3a7a513fcbb80ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:19:42 GMT
ENV container oci
# Wed, 04 Feb 2026 11:19:43 GMT
COPY dir:0c6fd0301db67da56e5ab3d7939a023e089cbf858b44dcb22c5b0ce99938dd88 in /      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:19:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:19:27Z" "org.opencontainers.image.created"="2026-02-04T11:19:27Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:19:27Z
# Thu, 05 Feb 2026 00:10:14 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 00:10:16 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:10:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 00:10:19 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 00:10:19 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 00:10:19 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 00:10:19 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.15 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 00:10:19 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.15 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 00:10:19 GMT
ARG MARIADB_VERSION=10.11.15
# Thu, 05 Feb 2026 00:10:19 GMT
ENV MARIADB_VERSION=10.11.15
# Thu, 05 Feb 2026 00:10:44 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 00:10:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 00:10:44 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 00:10:44 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 00:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:10:44 GMT
USER mysql
# Thu, 05 Feb 2026 00:10:44 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 00:10:44 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c11b287f01a25d7e01178301d68fea1b93f43698745b530d24cc120d13c00d`  
		Last Modified: Thu, 05 Feb 2026 00:11:05 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbee02b1ed0560b061f3a4627a4c725fdc4767500e73ba01cdd1b2fd4fcf50a`  
		Last Modified: Thu, 05 Feb 2026 00:11:05 GMT  
		Size: 2.0 MB (2000434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d63219a4300b5a46ecde53ef180dbaffbc80a07f736cb2d49ffcc36adb9e58`  
		Last Modified: Thu, 05 Feb 2026 00:11:05 GMT  
		Size: 6.1 MB (6145283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1fd7ec6e50098b99963049ca0a87fbb06ebee414de7f2c09d60d6a57e03a21`  
		Last Modified: Thu, 05 Feb 2026 00:11:05 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f23e3c129eacc399949e04a89e4bb888dcc58020e0ede9013732853cf8700a`  
		Last Modified: Thu, 05 Feb 2026 00:11:06 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca031e60b2455e6593e96cb9f26ee2d40b3a0a54385c7d42846d680337e1c075`  
		Last Modified: Thu, 05 Feb 2026 00:11:09 GMT  
		Size: 115.4 MB (115425697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2630af44699977bbef7612b0a0a3d79e314036bab12f3a584f236c4c28c20e54`  
		Last Modified: Thu, 05 Feb 2026 00:11:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9792754469740c52e364632e5725a61dc7adc4fff7cecbc84d79979a53ac0b30`  
		Last Modified: Thu, 05 Feb 2026 00:11:07 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fba9df132dc32089d8c45d4e73c25cb77cb4651303c3e0a674e399d141cb98`  
		Last Modified: Thu, 05 Feb 2026 00:11:07 GMT  
		Size: 8.4 KB (8364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:c44045235cf10ead4d1993e61382333bf6ce2dbd4739a8e2e86fd5300cea114d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4758938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908d79bc69d8de9f91913948f3b6ffd275ceaab6d8129d9249f3323f87123870`

```dockerfile
```

-	Layers:
	-	`sha256:40d03ba1bb1a8fd9ab0b19d050bcf2bbcfd2110849eb1c8558c7aefab34826e9`  
		Last Modified: Thu, 05 Feb 2026 00:11:05 GMT  
		Size: 4.7 MB (4724908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9491e576fe8d0121093a223685b0c907aa4645825a8773d8461ef153b221476`  
		Last Modified: Thu, 05 Feb 2026 00:11:05 GMT  
		Size: 34.0 KB (34030 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d21cc768a0af14873526c5a4630c6da56905e49469d7935688b05d6575e7bf4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176600837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d84e80382231cf170c7f554b72a5d457c785b02d08a095eefc04067ca0f4181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:18:55 GMT
ENV container oci
# Wed, 04 Feb 2026 11:18:56 GMT
COPY dir:ac22932cb19e0040fdd682ddcf58eafa9048ed80bbb0d7207ce4b58b9e8c1ce2 in /      
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:18:56 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:fc9edd6729debe0b8fd283950946b54a98819aab2c1a7de7861de07a73ecdf6a in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:18:57 GMT
COPY file:fc9edd6729debe0b8fd283950946b54a98819aab2c1a7de7861de07a73ecdf6a in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:18:57 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:18:45Z" "org.opencontainers.image.created"="2026-02-04T11:18:45Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:18:45Z
# Thu, 05 Feb 2026 01:30:17 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 01:30:21 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 01:30:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 01:30:26 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 01:32:58 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 01:32:59 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 01:32:59 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.15 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 01:32:59 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.15 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 01:32:59 GMT
ARG MARIADB_VERSION=10.11.15
# Thu, 05 Feb 2026 01:32:59 GMT
ENV MARIADB_VERSION=10.11.15
# Thu, 05 Feb 2026 01:33:48 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 01:33:48 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 01:33:49 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 01:33:49 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 01:33:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 01:33:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 01:33:49 GMT
USER mysql
# Thu, 05 Feb 2026 01:33:49 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 01:33:49 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9453cd9cf4ac5c59d91e7e792edc9ae031294feb6835b6b8c1c7fe6c37f48881`  
		Last Modified: Wed, 04 Feb 2026 12:09:30 GMT  
		Size: 44.5 MB (44463451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fdfc2186db63b32861670fc405c63305768dcc1ad016cf5d689827441d6e3e`  
		Last Modified: Thu, 05 Feb 2026 01:32:40 GMT  
		Size: 4.8 KB (4758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466788a69a26f7f774b600fe25eaf09d0392ef78540c27ccd8f26abcedc230e7`  
		Last Modified: Thu, 05 Feb 2026 01:32:41 GMT  
		Size: 2.0 MB (1997879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbe9f1b3303eac2400e6f7332402a0a68d1bbfd3ecf1b2bb1cd5cd6915db181`  
		Last Modified: Thu, 05 Feb 2026 01:32:41 GMT  
		Size: 6.1 MB (6145036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f47113b1e50426ebf62e7d1736c6c6a7c0f75a12c51da252d721f44dbb2ac3d`  
		Last Modified: Thu, 05 Feb 2026 01:34:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce01652734bdc5fd8e3bc5cd819074c783c5d43ff782e694a54b31e968033839`  
		Last Modified: Thu, 05 Feb 2026 01:34:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932d199c474d854296db77882083674969dbf56bf1b84bcb73d5bb7979d88584`  
		Last Modified: Thu, 05 Feb 2026 01:34:40 GMT  
		Size: 124.0 MB (123976545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e7425d50a9af95ac74490cd9defd4557af8ea90d068595f97f422a17a9433e`  
		Last Modified: Thu, 05 Feb 2026 01:34:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1961ed25a7385394e63837c7ea94d434c7cb9bd5837ca38cbcfe37c098e37618`  
		Last Modified: Thu, 05 Feb 2026 01:34:38 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a3470a73a9b62cee636daa451a7075566ba9e0c62e09b2b58ceae70329fe1e`  
		Last Modified: Thu, 05 Feb 2026 01:34:38 GMT  
		Size: 8.4 KB (8362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:1888096d5f762a1d9e75a75672e4b4db6b49db11e9bfa8818aaf800740d04244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4754305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7cb99a3c9903fff6953f729ecdbf3dd37092980fd1e054e8fa4c0544af649b`

```dockerfile
```

-	Layers:
	-	`sha256:f609acced590561a9a358225507813347b3f69abbdd98c5655fa096b00f65437`  
		Last Modified: Thu, 05 Feb 2026 01:34:37 GMT  
		Size: 4.7 MB (4720399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77cfc2d500680b21c3de54c0c84e4498ede0e68ba7c47ba86bc966f6971889b`  
		Last Modified: Thu, 05 Feb 2026 01:34:37 GMT  
		Size: 33.9 KB (33906 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:87a725dc9c9868306f2bcd19e9355008aa1a87e6aa0c3fc08b915ab554f640ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163819487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5d9368dcf866b36312fc08589f1752116d7d4fef0f8a2d93fe57eef62168ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:28:10 GMT
ENV container oci
# Wed, 04 Feb 2026 11:28:10 GMT
COPY dir:ed1f066185517b0a2e4ef9432478916be75ee58442b799a2d0b87cd51ad8226a in /      
# Wed, 04 Feb 2026 11:28:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:28:10 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:28:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:28:11 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:28:11 GMT
COPY file:696c21c97fda61d0f3f09e274ba392676dba268826f34e2eb4e63f66e68bb97f in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:28:11 GMT
COPY file:696c21c97fda61d0f3f09e274ba392676dba268826f34e2eb4e63f66e68bb97f in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:28:11 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:27:14Z" "org.opencontainers.image.created"="2026-02-04T11:27:14Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:27:14Z
# Thu, 05 Feb 2026 00:11:12 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Thu, 05 Feb 2026 00:11:14 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:11:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 00:11:17 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 00:11:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Thu, 05 Feb 2026 00:11:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Thu, 05 Feb 2026 00:11:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.15 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Thu, 05 Feb 2026 00:11:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.15 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 05 Feb 2026 00:11:24 GMT
ARG MARIADB_VERSION=10.11.15
# Thu, 05 Feb 2026 00:11:24 GMT
ENV MARIADB_VERSION=10.11.15
# Thu, 05 Feb 2026 00:11:47 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Thu, 05 Feb 2026 00:11:47 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 00:11:47 GMT
# ARGS: MARIADB_VERSION=10.11.15
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Feb 2026 00:11:47 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 05 Feb 2026 00:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:11:47 GMT
USER mysql
# Thu, 05 Feb 2026 00:11:47 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 05 Feb 2026 00:11:47 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a3073672938ee024c2e2b6308a166357e08b9d63db19f1301982940b3e05b9c5`  
		Last Modified: Wed, 04 Feb 2026 12:09:20 GMT  
		Size: 38.1 MB (38133403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc857adc34860751600713e71a79cd4e85765403d8d3a3f1a5eb8adf7564f1ff`  
		Last Modified: Thu, 05 Feb 2026 00:12:11 GMT  
		Size: 4.8 KB (4758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb95829bbf6a7e2ea0de11e9889097416bd46f3624997fdf8eaf0b006e1bb51`  
		Last Modified: Thu, 05 Feb 2026 00:12:11 GMT  
		Size: 2.0 MB (2012017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdd66c7b06e61cef967b5e0e2d653f86112a1f0059646059b57324880c89a93`  
		Last Modified: Thu, 05 Feb 2026 00:12:12 GMT  
		Size: 6.2 MB (6165491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e5f19953570b7adc103756e38be1afc129319300b18c2d7f992f6d98a272b6`  
		Last Modified: Thu, 05 Feb 2026 00:12:17 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14645fdd8732ffbc2bfd65c00c8f829a28e0842e00bca8df48329cfe3aafbc1d`  
		Last Modified: Thu, 05 Feb 2026 00:12:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51e1025e5fad84e24b3ad8b73fdb2d6beaedf2bc2d76fb14ee32278d27c3cfa`  
		Last Modified: Thu, 05 Feb 2026 00:12:23 GMT  
		Size: 117.5 MB (117490658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93b9c8e0b2ab6ee7f23dc3c875f7a3c9974d391ec6aba4493efe1c97d4c1ccf`  
		Last Modified: Thu, 05 Feb 2026 00:12:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7e8fb13f7aac1a8abb5957028d2b47058bf943b24c41822ee4f885b0346b37`  
		Last Modified: Thu, 05 Feb 2026 00:12:18 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cff21e38b73843836f8ad249357d636cfc7ad48f63e202ed626159dd5b3b26`  
		Last Modified: Thu, 05 Feb 2026 00:12:19 GMT  
		Size: 8.4 KB (8363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:5c61bc3f7705f8e46ae5febfa08f858b103bda326d627062d25049da8a98e49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4748677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46a683798fa9c8d8a02e26a31a410401db0c0277898447f237196a1ad5ddd59`

```dockerfile
```

-	Layers:
	-	`sha256:eac6d8953f8492ccb41bdc83330f7972c18f08b49bd0f53b0675deb0fda97ed8`  
		Last Modified: Thu, 05 Feb 2026 00:12:18 GMT  
		Size: 4.7 MB (4714831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc943eca955ceb7ba28ffbbc42d789e52666f0d8afcc3d4e006b8c97fe212bcb`  
		Last Modified: Thu, 05 Feb 2026 00:12:18 GMT  
		Size: 33.8 KB (33846 bytes)  
		MIME: application/vnd.in-toto+json
