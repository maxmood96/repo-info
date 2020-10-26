## `percona:psmdb-3.6`

```console
$ docker pull percona@sha256:ac265b4ec8fed1766dc22260cdc52fdbdf2bedd529ab621abcf9b20f8717178d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `percona:psmdb-3.6` - linux; amd64

```console
$ docker pull percona@sha256:021a211cedfb0683d3594d6309a19a1eb2f817435bb2e33d3b90d332963f6075
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157653105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638083383fc6ffa940c5a98ec2fbc9b2cce9a3244d00eaf266c00c07f0732121`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 10 Aug 2020 18:19:49 GMT
ADD file:538afc0c5c964ce0dde0141953a4dcf03c2d993c5989c92e7fee418e9305e2a3 in / 
# Mon, 10 Aug 2020 18:19:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809
# Mon, 10 Aug 2020 18:19:49 GMT
CMD ["/bin/bash"]
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.label-schema.schema-version=1.0
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.label-schema.name=Percona Server for MongoDB
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.label-schema.vendor=Percona
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.label-schema.description=Percona Server for MongoDB is our free and open-source drop-in replacement for MongoDB Community Edition. It offers all the features and benefits of MongoDB Community Edition, plus additional enterprise-grade functionality.
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.label-schema.license=SSPLv1
# Fri, 04 Sep 2020 19:25:41 GMT
LABEL org.opencontainers.image.title=Percona Server for MongoDB
# Fri, 04 Sep 2020 19:25:42 GMT
LABEL org.opencontainers.image.vendor=Percona
# Fri, 04 Sep 2020 19:25:42 GMT
LABEL org.opencontainers.image.description=Percona Server for MongoDB is our free and open-source drop-in replacement for MongoDB Community Edition. It offers all the features and benefits of MongoDB Community Edition, plus additional enterprise-grade functionality.
# Fri, 04 Sep 2020 19:25:42 GMT
LABEL org.opencontainers.image.license=SSPLv1
# Fri, 04 Sep 2020 19:25:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 26 Oct 2020 17:24:28 GMT
ENV PSMDB_VERSION=3.6.20-9.0
# Mon, 26 Oct 2020 17:24:28 GMT
ENV OS_VER=el8
# Mon, 26 Oct 2020 17:24:28 GMT
ENV FULL_PERCONA_VERSION=3.6.20-9.0.el8
# Mon, 26 Oct 2020 17:24:28 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 26 Oct 2020 17:24:28 GMT
LABEL org.label-schema.schema-version=3.6.20-9.0
# Mon, 26 Oct 2020 17:24:29 GMT
LABEL org.opencontainers.image.version=3.6.20-9.0
# Mon, 26 Oct 2020 17:24:35 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     dnf install -y /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Mon, 26 Oct 2020 17:24:50 GMT
RUN set -ex;     dnf install -y         dnf-utils         shadow-utils         curl         procps-ng         jq         oniguruma         Percona-Server-MongoDB-36-shell-${FULL_PERCONA_VERSION}         Percona-Server-MongoDB-36-mongos-${FULL_PERCONA_VERSION};         repoquery -a --location             policycoreutils                 | xargs curl -Lf -o /tmp/policycoreutils.rpm;         repoquery -a --location             Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}                 | xargs curl -Lf -o /tmp/Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}.rpm;         rpm -iv /tmp/policycoreutils.rpm /tmp/Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}.rpm --nodeps;                 rm -rf /tmp/policycoreutils.rpm /tmp/Percona-Server-MongoDB-36-server-${FULL_PERCONA_VERSION}.rpm;         dnf remove -y dnf-utils;         dnf clean all;         rm -rf /var/cache/dnf /data/db && mkdir -p /data/db;         chown -R 1001:0 /data/db
# Mon, 26 Oct 2020 17:24:50 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Mon, 26 Oct 2020 17:24:51 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Mon, 26 Oct 2020 17:24:51 GMT
RUN cp /usr/share/doc/Percona-Server-MongoDB-36-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Mon, 26 Oct 2020 17:24:53 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Mon, 26 Oct 2020 17:24:54 GMT
VOLUME [/data/db]
# Mon, 26 Oct 2020 17:24:54 GMT
COPY file:36bd7798a7bd236f79a692385b6877519fd05ff40f92de87cb1d5c527c35d799 in /entrypoint.sh 
# Mon, 26 Oct 2020 17:24:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Oct 2020 17:24:54 GMT
EXPOSE 27017
# Mon, 26 Oct 2020 17:24:54 GMT
USER 1001
# Mon, 26 Oct 2020 17:24:54 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3c72a8ed68140139e483fe7368ae4d9651422749e91483557cbd5ecf99a96110`  
		Last Modified: Mon, 10 Aug 2020 18:21:27 GMT  
		Size: 74.9 MB (74868121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23fc827a496eb3c077fcef59e088800bc6f1cbe54185087987e552096bf8e49a`  
		Last Modified: Mon, 26 Oct 2020 17:25:29 GMT  
		Size: 18.5 MB (18498764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b1b93cdcac2da2df8793a9ded026af624430baa62e7e242d7715d5fbc2c376`  
		Last Modified: Mon, 26 Oct 2020 17:25:36 GMT  
		Size: 56.1 MB (56127594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb0bf69fb72ec24a3c6ea3918a369693b9f22048e24b09d6d605a5f59b2a1ee`  
		Last Modified: Mon, 26 Oct 2020 17:25:26 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acc9f9ac9b27006e9d64b494581a0db18c4a42887de0db19c972e0bbc696400`  
		Last Modified: Mon, 26 Oct 2020 17:25:26 GMT  
		Size: 4.1 KB (4073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0120f731f7d28eae0430bd6d7a3e579bdcee8f03f0c283c6fb90338ba5f6558`  
		Last Modified: Mon, 26 Oct 2020 17:25:26 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040f7b053d9753e7f7f28c49ddafc840415d9f8f85e6aee3095828e5168d5f4`  
		Last Modified: Mon, 26 Oct 2020 17:25:42 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599d792bd8774760855965a0257b798170d683054b6c043d9b3b1116fba33306`  
		Last Modified: Mon, 26 Oct 2020 17:25:26 GMT  
		Size: 4.5 KB (4542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
