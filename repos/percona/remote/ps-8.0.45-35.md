## `percona:ps-8.0.45-35`

```console
$ docker pull percona@sha256:8b4aa3d5171660f4040e96efdb76b7dab6c8e1faf4a657b4f3713968b3171910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `percona:ps-8.0.45-35` - linux; amd64

```console
$ docker pull percona@sha256:e85fe46963455bcdf80bc2888311b3c3f9ac178fafa757049eac53f9b3765b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428638267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5f3725fa3c6afe1199c337edc4ce34a6d557fd47d3dc8f4c4bd4d288fa631b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:26:37 GMT
ENV container oci
# Mon, 13 Apr 2026 18:26:38 GMT
COPY dir:5191e1ce97881b91cd281225b61de5b907dbc286c69b6681e228608a9d6bab0b in /      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:26:38 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:39 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:26:26Z" "org.opencontainers.image.created"="2026-04-13T18:26:26Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:26:26Z
# Tue, 14 Apr 2026 20:44:30 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 14 Apr 2026 20:44:30 GMT
RUN set -ex;     groupadd -g 1001 mysql;     useradd -u 1001 -r -g 1001 -s /sbin/nologin         -m -c "Default Application User" mysql # buildkit
# Tue, 14 Apr 2026 20:44:30 GMT
ENV PS_VERSION=8.0.45-36.1
# Tue, 14 Apr 2026 20:44:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1
# Tue, 14 Apr 2026 20:44:30 GMT
ENV OS_VER=el9
# Tue, 14 Apr 2026 20:44:30 GMT
ENV FULL_PERCONA_VERSION=8.0.45-36.1.el9
# Tue, 14 Apr 2026 20:44:30 GMT
ENV FULL_MYSQL_SHELL_VERSION=8.0.45-1.el9
# Tue, 14 Apr 2026 20:44:30 GMT
ENV PS_REPO=testing
# Tue, 14 Apr 2026 20:44:30 GMT
ENV PS_TELEMETRY_VERSION=8.0.45-36-1
# Tue, 14 Apr 2026 20:44:30 GMT
ENV CALL_HOME_DOWNLOAD_SHA256=5e84d2f1a5d57f44c46e6a1f16794d649d3de09fe8021f0294bc321c89e51068
# Tue, 14 Apr 2026 20:44:30 GMT
ENV KEY_RPM_DOWNLOAD_SHA256=fcf0eab4f05a1c0de6363ac4b707600a27a9d774e9b491059e59e6921b255a84
# Tue, 14 Apr 2026 20:44:30 GMT
ENV CALL_HOME_VERSION=0.1
# Tue, 14 Apr 2026 20:44:30 GMT
ARG PERCONA_TELEMETRY_DISABLE=1
# Tue, 14 Apr 2026 20:44:36 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4D1BB29D63D98E422B2113B19334A25F8507EFA5 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 4D1BB29D63D98E422B2113B19334A25F8507EFA5 > ${GNUPGHOME}/PERCONA-PACKAGING-KEY;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/PERCONA-PACKAGING-KEY ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     microdnf install -y findutils;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release disable all;     percona-release enable ps-80 ${PS_REPO};     percona-release enable mysql-shell ${PS_REPO};     curl -O https://dl.fedoraproject.org/pub/epel/RPM-GPG-KEY-EPEL-9;     echo "$KEY_RPM_DOWNLOAD_SHA256 RPM-GPG-KEY-EPEL-9" | sha256sum --strict --check;     rpm --import RPM-GPG-KEY-EPEL-9;     curl -Lf -o /tmp/jemalloc.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/j/jemalloc-5.2.1-2.el9.x86_64.rpm;     curl -Lf -o /tmp/gflags.rpm https://rpmfind.net/linux/epel/9/Everything/x86_64/Packages/g/gflags-2.2.2-9.el9.x86_64.rpm;     rpmkeys --checksig /tmp/gflags.rpm /tmp/jemalloc.rpm;     rpm -i /tmp/jemalloc.rpm;     rpm -i /tmp/gflags.rpm;     rm -f /tmp/gflags.rpm /tmp/jemalloc.rpm # buildkit
# Tue, 14 Apr 2026 20:45:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     rpm -e --nodeps tzdata;     microdnf -y install         hostname         tzdata         jemalloc         which         cracklib-dicts         tar         policycoreutils;     microdnf -y update         libnghttp2         openssh         python3-setuptools-wheel         krb5-libs         pam         python3;         microdnf -y install         percona-server-server-${FULL_PERCONA_VERSION}         percona-server-devel-${FULL_PERCONA_VERSION}         percona-server-rocksdb-${FULL_PERCONA_VERSION}         percona-icu-data-files-${FULL_PERCONA_VERSION}         percona-mysql-shell-${FULL_MYSQL_SHELL_VERSION};     microdnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /var/lib/mysql # buildkit
# Tue, 14 Apr 2026 20:45:03 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -ex;     /usr/bin/install -m 0775 -o mysql -g root -d /var/lib/mysql /var/run/mysqld /docker-entrypoint-initdb.d; 	find /etc/my.cnf /etc/my.cnf.d -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user)/#&/'; 	echo '!includedir /etc/my.cnf.d' >> /etc/my.cnf; 	printf '[mysqld]\nhost_cache_size=0\nskip-name-resolve\n' > /etc/my.cnf.d/docker.cnf; 	/usr/bin/install -m 0664 -o mysql -g root /dev/null /etc/sysconfig/mysql; 	echo "LD_PRELOAD=/usr/lib64/libjemalloc.so.1" >> /etc/sysconfig/mysql; 	echo "THP_SETTING=never" >> /etc/sysconfig/mysql; 	chown -R mysql:root /etc/my.cnf /etc/my.cnf.d; 	chmod -R ug+rwX /etc/my.cnf /etc/my.cnf.d # buildkit
# Tue, 14 Apr 2026 20:45:03 GMT
VOLUME [/var/lib/mysql /var/log/mysql]
# Tue, 14 Apr 2026 20:45:04 GMT
# ARGS: PERCONA_TELEMETRY_DISABLE=1
RUN set -eux;     curl -fL "https://github.com/Percona-Lab/telemetry-agent/archive/refs/tags/phase-$CALL_HOME_VERSION.tar.gz" -o "phase-$CALL_HOME_VERSION.tar.gz";     echo "$CALL_HOME_DOWNLOAD_SHA256 phase-$CALL_HOME_VERSION.tar.gz" | sha256sum --strict --check;     tar -xvf phase-$CALL_HOME_VERSION.tar.gz;     cp telemetry-agent-phase-$CALL_HOME_VERSION/call-home.sh .;    rm -rf telemetry-agent-phase-$CALL_HOME_VERSION phase-$CALL_HOME_VERSION.tar.gz;     chmod a+rx /call-home.sh;     mkdir -p /usr/local/percona;     chown mysql:mysql /usr/local/percona # buildkit
# Tue, 14 Apr 2026 20:45:04 GMT
ENV CALL_HOME_OPTIONAL_PARAMS= -s el9
# Tue, 14 Apr 2026 20:45:04 GMT
COPY ps-entry-dockerhub.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:04 GMT
USER mysql
# Tue, 14 Apr 2026 20:45:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 14 Apr 2026 20:45:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7a8ea8eaa1a83b7e274dac6fe8542849c3782921090ccfcdd6da2d1350189d`  
		Last Modified: Tue, 14 Apr 2026 20:45:47 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9251eaa73fceac4302bcbd37f1b94771e43ebfbae93492ab92fe40088b41635`  
		Last Modified: Tue, 14 Apr 2026 20:45:47 GMT  
		Size: 9.2 MB (9217188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a998fd064d5f2a32c02edf03c1ea197d0ad9dd5f630dd3a37acef730a974f1`  
		Last Modified: Tue, 14 Apr 2026 20:45:55 GMT  
		Size: 379.4 MB (379394790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3affe44d86faa341e9aac754954cb35dff29a1e8446f825a10f393a9fac10fff`  
		Last Modified: Tue, 14 Apr 2026 20:45:48 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50b638bca1acfa22c9df27b47cdd33178e29878547183af57d8a6d0708e60b5`  
		Last Modified: Tue, 14 Apr 2026 20:45:49 GMT  
		Size: 4.0 KB (3958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea76b3d39a310e3d17d1c3c432b995991fc1a34f6d3ce655ef41e2e9abb89936`  
		Last Modified: Tue, 14 Apr 2026 20:45:49 GMT  
		Size: 3.3 KB (3282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `percona:ps-8.0.45-35` - unknown; unknown

```console
$ docker pull percona@sha256:cc645dc4bbb6f98eea89d4b7d090be38b684648a55a7b0c12887018142c31a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1a54f13d72cba008b66d0800164ffc24d26bfa7a8f9940cdc9f2a2d43bc6a7`

```dockerfile
```

-	Layers:
	-	`sha256:a18b06c3b46023e4d7f4cffe37298375fbba7278bb2b2be1bbba36dc65dbd15c`  
		Last Modified: Tue, 14 Apr 2026 20:45:47 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json
