## `mariadb:10-ubi`

```console
$ docker pull mariadb@sha256:647c5ad5b87810ca80a1c644b5e3d677f6a0894ed77e6610817cd04a7c0d9bcc
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
$ docker pull mariadb@sha256:37010c91f0be226b09da46e1a37cda4c2c5aebba4dc63aa505e97f74d784f677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166181679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a52d94e523fba1e9b2494df164d1cfe750ce6df3e89bf1149e9949d383b4ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:29:53 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Wed, 08 Apr 2026 17:29:54 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:29:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Apr 2026 17:29:57 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Apr 2026 17:29:57 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Wed, 08 Apr 2026 17:29:57 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Wed, 08 Apr 2026 17:29:57 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.16 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 08 Apr 2026 17:29:57 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 08 Apr 2026 17:29:57 GMT
ARG MARIADB_VERSION=10.11.16
# Wed, 08 Apr 2026 17:29:57 GMT
ENV MARIADB_VERSION=10.11.16
# Wed, 08 Apr 2026 17:30:22 GMT
# ARGS: MARIADB_VERSION=10.11.16
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 08 Apr 2026 17:30:22 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Apr 2026 17:30:22 GMT
# ARGS: MARIADB_VERSION=10.11.16
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 08 Apr 2026 17:30:23 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 08 Apr 2026 17:30:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:30:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:30:23 GMT
USER mysql
# Wed, 08 Apr 2026 17:30:23 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 08 Apr 2026 17:30:23 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1cf6488e73bc15cac9c1890eef6eaa84e69823fe4a964c228701a438902259`  
		Last Modified: Wed, 08 Apr 2026 17:30:43 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5be8e2d62de3508926c67edf268a8d2fe0439bbc48fceb906e72f81ba32310`  
		Last Modified: Wed, 08 Apr 2026 17:30:43 GMT  
		Size: 2.0 MB (1994113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6fd41cf189b32113e353da558f7165666f6a7b0f4978996053b9ab687e9544`  
		Last Modified: Wed, 08 Apr 2026 17:30:44 GMT  
		Size: 7.2 MB (7210557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe96a72b3c3c4af1deaf81d1a5ea7b0680baca1839fafa053581b0c3c1e64f5`  
		Last Modified: Wed, 08 Apr 2026 17:30:44 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb104bfa1d1a0e43632489e311be0034260b781259e0689e649fbe447bc16bf6`  
		Last Modified: Wed, 08 Apr 2026 17:30:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c53954094f875158ea0a440c7f091761953a92b0c44d8763307438bf4a35a9b`  
		Last Modified: Wed, 08 Apr 2026 17:30:53 GMT  
		Size: 117.0 MB (116976441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7eae148f2f63ce18d5d1e9b01ff8fa53db686175a94774e70b08f5d02a9dc0`  
		Last Modified: Wed, 08 Apr 2026 17:30:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3defd7eb3a474ed681b90663494befec24b92148f76509a97342ae4258b58f08`  
		Last Modified: Wed, 08 Apr 2026 17:30:46 GMT  
		Size: 4.0 KB (4015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809023250a1c6d0cbebf4aa5ec7afdd6a3ee4c0f3b49bb3694fb9a68f2797d3b`  
		Last Modified: Wed, 08 Apr 2026 17:30:46 GMT  
		Size: 8.4 KB (8363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:b5cb5a2ad9d4dcc07c92f8b95a4443f67f45d5da855861bc24a80b33c1dc32f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506e9200f3b3d70075e1991b637ec239b34b123ef0070d6323e50322c8646bbe`

```dockerfile
```

-	Layers:
	-	`sha256:0c5d988570c1127f9144a82f877ad73deb93e7617e7a230032abc7e9013ff326`  
		Last Modified: Wed, 08 Apr 2026 17:30:44 GMT  
		Size: 4.7 MB (4725337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cc9f4ad81f6656532f1cc0917de3a8794a1d0170aaec597ee858f950f8fd0bd`  
		Last Modified: Wed, 08 Apr 2026 17:30:44 GMT  
		Size: 33.9 KB (33869 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a1f564570b5cb130369e491adad96214aab56211e83f0f7b88ec4f06879a06fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161481675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6d73c5465444c01838726eee6f4a34987c12d2fa802b35f78f46a2c47d2c35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:55:31 GMT
ENV container oci
# Wed, 08 Apr 2026 04:55:32 GMT
COPY dir:e3968b666ccf8b1da827a1f934e7d66b38ad6335b0bf20a2a01583a6f9f3fdaa in /      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:55:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:33 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:55:18Z" "org.opencontainers.image.created"="2026-04-08T04:55:18Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:55:18Z
# Wed, 08 Apr 2026 17:29:19 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Wed, 08 Apr 2026 17:29:20 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:29:24 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Apr 2026 17:29:24 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Apr 2026 17:29:24 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Wed, 08 Apr 2026 17:29:24 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Wed, 08 Apr 2026 17:29:24 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.16 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 08 Apr 2026 17:29:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 08 Apr 2026 17:29:24 GMT
ARG MARIADB_VERSION=10.11.16
# Wed, 08 Apr 2026 17:29:24 GMT
ENV MARIADB_VERSION=10.11.16
# Wed, 08 Apr 2026 17:29:48 GMT
# ARGS: MARIADB_VERSION=10.11.16
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 08 Apr 2026 17:29:48 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Apr 2026 17:29:48 GMT
# ARGS: MARIADB_VERSION=10.11.16
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 08 Apr 2026 17:29:48 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 08 Apr 2026 17:29:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:29:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:29:48 GMT
USER mysql
# Wed, 08 Apr 2026 17:29:48 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 08 Apr 2026 17:29:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:1ffb0d1826b0600c6d4836c7ada23756af4c1475452e12ce1bed713d58738262`  
		Last Modified: Wed, 08 Apr 2026 05:41:58 GMT  
		Size: 38.2 MB (38200278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b36c452974fb96a6f72f92447eec9f108f7c905fc33df8ff2d98d5020eaf54`  
		Last Modified: Wed, 08 Apr 2026 17:30:09 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb2bff3e42b42a4719de5b302a7b432fd2abceb20d0663df3593a5be3ed0b37`  
		Last Modified: Wed, 08 Apr 2026 17:30:10 GMT  
		Size: 2.0 MB (1988285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d017eebe4a4e294e0ae53da8d4e8a5e94eb79137724d9e74a48aae04e1281ef4`  
		Last Modified: Wed, 08 Apr 2026 17:30:10 GMT  
		Size: 6.2 MB (6152601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0e5b87374b48eb27e1bd27c61bc899161f75cdd4017d295b8c805f1c8db2e9`  
		Last Modified: Wed, 08 Apr 2026 17:30:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8355fc2beccbfda71f5f74599e114f918129cefad5ef71f762b992b83e902cd4`  
		Last Modified: Wed, 08 Apr 2026 17:30:11 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347875e1687bfb30742b9f01e090b6d5c1021c56b96195071d5b1e88bb865d93`  
		Last Modified: Wed, 08 Apr 2026 17:30:14 GMT  
		Size: 115.1 MB (115122592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26af255b9f7ab0af031929234968b5eb2d2ee4a1b827b4d5877242cb4e205434`  
		Last Modified: Wed, 08 Apr 2026 17:30:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1ec7a54f7f289a483aefc4627e1f6d80e04331dccf9387610b736444eefc9c`  
		Last Modified: Wed, 08 Apr 2026 17:30:12 GMT  
		Size: 4.0 KB (4013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdcfa86c663a390cc8ed223f095c1c26c131ee31968aa9951efb8b9f811d515`  
		Last Modified: Wed, 08 Apr 2026 17:30:12 GMT  
		Size: 8.4 KB (8360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:72e272d0de204f457ad6ec7df6d63cb7ba45ea7e02039ec1819d753e56489319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4758196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509004eba125af23f0540ac8aeee3746f1a49cd2cdc8dca1cbfbb25540075486`

```dockerfile
```

-	Layers:
	-	`sha256:b1766633f0ff779b0587476929cd10afffcd03e319895f22ef1e8a1b407abb03`  
		Last Modified: Wed, 08 Apr 2026 17:30:10 GMT  
		Size: 4.7 MB (4724148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74946a62e62b28f778892068858b3e62a5a83c8f17baf2df5b2c126ca5bc6bd`  
		Last Modified: Wed, 08 Apr 2026 17:30:10 GMT  
		Size: 34.0 KB (34048 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; ppc64le

```console
$ docker pull mariadb@sha256:abe2ec5043d2898d91f96a0228a11b78145c08e23671bf5de9584fc33957a117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176190499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abccd806364916bc0dea32b5b088b21fb49d77b9f1c34f45860ff07c4eb8efe1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:54:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:54:19 GMT
ENV container oci
# Wed, 08 Apr 2026 04:54:20 GMT
COPY dir:436d133f1cdcc884037448e774a24a829aca74f2e3df9ed98967bc293872db72 in /      
# Wed, 08 Apr 2026 04:54:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:54:20 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:54:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:54:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:54:20 GMT
COPY file:3d096e486f3f704f5a85bb466b49e2b6383b940a165abc05b73dce12cd4502bf in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:54:20 GMT
COPY file:3d096e486f3f704f5a85bb466b49e2b6383b940a165abc05b73dce12cd4502bf in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:54:21 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:54:09Z" "org.opencontainers.image.created"="2026-04-08T04:54:09Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:54:09Z
# Wed, 08 Apr 2026 17:45:41 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Wed, 08 Apr 2026 17:45:45 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:45:51 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Apr 2026 17:45:51 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Apr 2026 17:47:57 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Wed, 08 Apr 2026 17:47:58 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Wed, 08 Apr 2026 17:47:58 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.16 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 08 Apr 2026 17:47:58 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 08 Apr 2026 17:47:58 GMT
ARG MARIADB_VERSION=10.11.16
# Wed, 08 Apr 2026 17:47:58 GMT
ENV MARIADB_VERSION=10.11.16
# Wed, 08 Apr 2026 17:50:08 GMT
# ARGS: MARIADB_VERSION=10.11.16
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 08 Apr 2026 17:50:08 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Apr 2026 17:50:09 GMT
# ARGS: MARIADB_VERSION=10.11.16
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 08 Apr 2026 17:50:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 08 Apr 2026 17:50:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:50:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:50:10 GMT
USER mysql
# Wed, 08 Apr 2026 17:50:10 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 08 Apr 2026 17:50:10 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3e558ab952e7353c7098da86d39e696cc812d91e36d37e1b280a09e42c0fa29e`  
		Last Modified: Wed, 08 Apr 2026 06:11:41 GMT  
		Size: 44.5 MB (44454533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aa971d8a13f7bfabf188a9d5ee95d7cf1b2fa2969afb038a9607f9e7e7b60c`  
		Last Modified: Wed, 08 Apr 2026 17:47:40 GMT  
		Size: 4.8 KB (4760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6e757da2f5867fed2d37337e6700c400f90682e0dda53fdebc0d4de7673239`  
		Last Modified: Wed, 08 Apr 2026 17:47:40 GMT  
		Size: 2.0 MB (1983902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4294de825d2e9ccb80239dd94727ca92542f8f38486b77c20852493c31c1d`  
		Last Modified: Wed, 08 Apr 2026 17:47:41 GMT  
		Size: 6.1 MB (6141439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8f805a378b698d7dea92559f22931db893c0177b2ed97bbb9a942cf21607fa`  
		Last Modified: Wed, 08 Apr 2026 17:49:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c84a76ecd8dae007a0dcc445aaf3bf10061a09dfe8a899a54566569ea14511`  
		Last Modified: Wed, 08 Apr 2026 17:50:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22bb6732d0493bf9715ee08995ed01c608fa0bca9f2f60ee6acbea4aac18606`  
		Last Modified: Wed, 08 Apr 2026 17:50:59 GMT  
		Size: 123.6 MB (123592699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb8e0df8a61e67edbc4509faec1a25f76bc19a00d2afaf436265a3c95a2fc96`  
		Last Modified: Wed, 08 Apr 2026 17:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566a54bd788f5384eaec8fe792c8f2db6c34a26715d267d082d9355b91097b49`  
		Last Modified: Wed, 08 Apr 2026 17:50:54 GMT  
		Size: 4.0 KB (4015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9780746bf3e947efe9f8e433ba6f083190e7ac3c887793740bb790a0563ec698`  
		Last Modified: Wed, 08 Apr 2026 17:50:55 GMT  
		Size: 8.4 KB (8364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:1cd90dbc839f255965adde5a6a8884a7ddba520f34947a5b9148fb058d621b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4753566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709564ccae25a0c8787192ccdb3647dc67f360cdb0d2411c08e8cab241a2718a`

```dockerfile
```

-	Layers:
	-	`sha256:1db0ba6440cba4f01ba4ec34af184ecfe47dce05aeed972261e313fd1f2aae22`  
		Last Modified: Wed, 08 Apr 2026 17:50:54 GMT  
		Size: 4.7 MB (4719639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ef1c5f9831a0feed263d2b30051f3925557aae2c6c2a4db57fb98b4c1e1fc85`  
		Last Modified: Wed, 08 Apr 2026 17:50:53 GMT  
		Size: 33.9 KB (33927 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-ubi` - linux; s390x

```console
$ docker pull mariadb@sha256:48641f0cc8fb2cb852beaff8cb821b4d7c1c4a75ee040219666c9438df230f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163450480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bd1367525d3837460f95d38913efd479812af0925ba67192792ac915acfb9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:57:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:57:30 GMT
ENV container oci
# Wed, 08 Apr 2026 04:57:31 GMT
COPY dir:df6bb403ebf6f62a05d743be5f30411253e036d1b5e6d5fe4a30348c86682080 in /      
# Wed, 08 Apr 2026 04:57:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:57:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:57:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:57:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:57:31 GMT
COPY file:c085a9f1d8e36293754a8d06efb027a09ad650ab224af3e4a6fe83d436836064 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:57:31 GMT
COPY file:c085a9f1d8e36293754a8d06efb027a09ad650ab224af3e4a6fe83d436836064 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:57:31 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:57:20Z" "org.opencontainers.image.created"="2026-04-08T04:57:20Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:57:20Z
# Wed, 08 Apr 2026 17:25:17 GMT
RUN sed -i -e '/\[ evp_properties \]/a default_properties = fips=yes'  -e '/opensslcnf.config/a .include = /etc/crypto-policies/back-ends/openssl_fips.config' -e '/\[provider_sect\]/a fips = fips_sect' /etc/pki/tls/openssl.cnf # buildkit
# Wed, 08 Apr 2026 17:25:20 GMT
RUN microdnf install -y shadow-utils && 	groupadd --gid 999 -r mysql && 	useradd -r -g mysql mysql --home-dir /var/lib/mysql --uid 999 && 	microdnf remove -y shadow-utils && 	microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:25:25 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Apr 2026 17:25:25 GMT
RUN set -eux; 	rpmArch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$rpmArch" in 		aarch64) dpkgArch='arm64' ;; 		armv7*) dpkgArch='armhf' ;; 		i686) dpkgArch='i386' ;; 		ppc64le) dpkgArch='ppc64el' ;; 		s390x|riscv64) dpkgArch=$rpmArch ;; 		x86_64) dpkgArch='amd64' ;; 		*) echo >&2 "error: unknown/unsupported architecture '$rpmArch'"; exit 1 ;; 	esac; 	curl --fail --location --output /usr/local/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch} ; 	curl --fail --location --output /usr/local/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-${dpkgArch}.asc; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	microdnf install -y gnupg2; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	chmod a+x /usr/local/bin/gosu; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Apr 2026 17:25:25 GMT
COPY --chmod=0644 docker.cnf /etc/my.cnf.d/ # buildkit
# Wed, 08 Apr 2026 17:25:25 GMT
COPY MariaDB.repo /etc/yum.repos.d/ # buildkit
# Wed, 08 Apr 2026 17:25:25 GMT
LABEL name=MariaDB Server vendor=MariaDB Community version=10.11.16 release=Refer to Annotations org.opencontainers.image.{revision,source} summary=MariaDB Database description=MariaDB Database for relational SQL
# Wed, 08 Apr 2026 17:25:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/redhat/ubi9-minimal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 08 Apr 2026 17:25:25 GMT
ARG MARIADB_VERSION=10.11.16
# Wed, 08 Apr 2026 17:25:25 GMT
ENV MARIADB_VERSION=10.11.16
# Wed, 08 Apr 2026 17:26:08 GMT
# ARGS: MARIADB_VERSION=10.11.16
RUN set -eux ; 	curl --fail https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9 --output /tmp/epelkey.txt ; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME ; 	gpg --batch --import /tmp/epelkey.txt ; 	gpg --batch --armor --export FF8AD1344597106ECE813B918A3872BF3228467C > /tmp/epelkey.txt ; 	rpmkeys --import /tmp/epelkey.txt ; 	curl --fail https://dl.fedoraproject.org/pub/epel/epel-release-latest-9.noarch.rpm --output /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -K /tmp/epel-release-latest-9.noarch.rpm ; 	rpm -ivh /tmp/epel-release-latest-9.noarch.rpm ; 	rm /tmp/epelkey.txt /tmp/epel-release-latest-9.noarch.rpm ; 	curl --fail https://archive.mariadb.org/PublicKey --output /tmp/MariaDB-Server-GPG-KEY ; 	gpg --batch --import /tmp/MariaDB-Server-GPG-KEY; 	gpg --batch --armor --export 177F4010FE56CA3336300305F1656F24C74CD1D8 > /tmp/MariaDB-Server-GPG-KEY ; 	rpmkeys --import /tmp/MariaDB-Server-GPG-KEY ; 	rm -rf "$GNUPGHOME" /tmp/MariaDB-Server-GPG-KEY ; 	unset GNUPGHOME ; 	microdnf update -y ; 	microdnf reinstall -y tzdata ; 	microdnf install -y procps-ng zstd xz gzip tar jemalloc gperftools-libs pwgen pv util-linux-core ; 	mkdir -p /etc/mysql/conf.d /etc/mysql/mariadb.conf.d/ /var/lib/mysql/mysql /run/mariadb /usr/lib64/galera ; 	chmod ugo+rwx,o+t /run/mariadb ; 	microdnf install -y MariaDB-backup-${MARIADB_VERSION}  MariaDB-server-${MARIADB_VERSION} ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib/libgalera_smm.so ; 	ln -s /usr/lib64/galera-4/libgalera_smm.so /usr/lib64/galera/libgalera_smm.so ; 	openssl list -providers | awk '/^\s*fips/{f=1} f && /status: active/{print "FIPS is active"; found=1; exit 0} END { if (!found) { print "FIPS is not active"; exit 1} }'; 	microdnf clean all ; 	rmdir /var/lib/mysql/mysql ; 	chown -R mysql:mysql /var/lib/mysql /run/mariadb ; 	mkdir /licenses ; 	ln -s /usr/share/doc/MariaDB-server-${MARIADB_VERSION}/COPYING /licenses/GPL-2 ; 	ln -s /usr/share/licenses /licenses/package-licenses ; 	ln -s Apache-2.0-license /licenses/gosu # buildkit
# Wed, 08 Apr 2026 17:26:08 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Apr 2026 17:26:08 GMT
# ARGS: MARIADB_VERSION=10.11.16
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 08 Apr 2026 17:26:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 08 Apr 2026 17:26:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:26:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:26:09 GMT
USER mysql
# Wed, 08 Apr 2026 17:26:09 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 08 Apr 2026 17:26:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:54db3bbd8a20aa62ac98659e9789851e1e6fd4f38d510a6df422467c1f72259e`  
		Last Modified: Wed, 08 Apr 2026 06:11:32 GMT  
		Size: 38.1 MB (38110884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be00374ca5aba344f814afa78808c47e5f76771b81e1b33c1e71a6b509a0191`  
		Last Modified: Wed, 08 Apr 2026 17:26:50 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5393b4ae1b0b307243c2f3f7a492336a91e1b9962f57c924c649d5e77871c1`  
		Last Modified: Wed, 08 Apr 2026 17:26:50 GMT  
		Size: 2.0 MB (2002155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4074f2a9ade6cdd8ee7b8a8a532ddc9f1f9618fe4e5af68d03302558c769e1d5`  
		Last Modified: Wed, 08 Apr 2026 17:26:51 GMT  
		Size: 6.2 MB (6161904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af273610b5a0d5d553f58154000c5eefed1b39fddba64d832cb6a692b13b1c46`  
		Last Modified: Wed, 08 Apr 2026 17:26:51 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3f1ff320b15e4d81f1307f87d1708eb73e2e99ef38c6e9afa2c4998e4eebf4`  
		Last Modified: Wed, 08 Apr 2026 17:26:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076b16d4e694d0ca5ca741f3c828e3d122afb8e852de50107dbab4b56a16450e`  
		Last Modified: Wed, 08 Apr 2026 17:26:55 GMT  
		Size: 117.2 MB (117157615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b08ae544652796a374e59af912266edc8e46a6df1b943a80c59079e6c86ab9e`  
		Last Modified: Wed, 08 Apr 2026 17:26:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa48a04b5988178e66ef3395e7b57811ba01548151f6df27b3c1ddad80d81e`  
		Last Modified: Wed, 08 Apr 2026 17:26:52 GMT  
		Size: 4.0 KB (4015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2420cd3257af9640ebd4b0ba3d902e7f7584a29667ccbfc75200dbf1c2f47ec`  
		Last Modified: Wed, 08 Apr 2026 17:26:53 GMT  
		Size: 8.4 KB (8360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-ubi` - unknown; unknown

```console
$ docker pull mariadb@sha256:3d10b99db43f46d410de2e0ced201bca1a75165e2966f46b18a6097106be6bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4747938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539c7ee40e041366ddf7ac2a0f0ac6a91454f862bba637ebdb68e0f822bc4dc`

```dockerfile
```

-	Layers:
	-	`sha256:4354d82ba7fcbc1fbe08759a3334da2e3b3a412874c0de498f93b4a3025be843`  
		Last Modified: Wed, 08 Apr 2026 17:26:50 GMT  
		Size: 4.7 MB (4714071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:509650f236d187a1ec1a2cf8ab9612faa1c1fd19cfa7bfa0a97b9b8ecf2f184f`  
		Last Modified: Wed, 08 Apr 2026 17:26:50 GMT  
		Size: 33.9 KB (33867 bytes)  
		MIME: application/vnd.in-toto+json
