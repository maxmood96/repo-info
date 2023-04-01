## `percona:psmdb-4.4`

```console
$ docker pull percona@sha256:de0c54ddb1aac51087e375ea8cb65fbdbf8eaac2f377f115e558fb4ac446d738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4` - linux; amd64

```console
$ docker pull percona@sha256:74757b2e87f154b2529e68cfa70fda43c84a83a081bd0e9c00f06940a10c5552
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198176770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf654e849e611d681c40c5ab420405c6a97aaad690cb2431a530bb3dd8974e93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 31 Mar 2023 22:28:30 GMT
ADD file:612f06c9f5ab410219b2415de45592033d4e9a8d5ce398134276a90224363fb7 in / 
# Fri, 31 Mar 2023 22:28:31 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:15:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 31 Mar 2023 23:16:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Fri, 31 Mar 2023 23:16:56 GMT
ENV PSMDB_VERSION=4.4.15-15
# Fri, 31 Mar 2023 23:16:56 GMT
ENV OS_VER=el8
# Fri, 31 Mar 2023 23:16:56 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Fri, 31 Mar 2023 23:16:56 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 31 Mar 2023 23:17:35 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 31 Mar 2023 23:17:35 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 31 Mar 2023 23:17:36 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 31 Mar 2023 23:17:36 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 31 Mar 2023 23:17:36 GMT
ENV GOSU_VERSION=1.11
# Fri, 31 Mar 2023 23:17:39 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 31 Mar 2023 23:17:41 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 31 Mar 2023 23:17:41 GMT
VOLUME [/data/db]
# Fri, 31 Mar 2023 23:17:42 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 31 Mar 2023 23:17:42 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 31 Mar 2023 23:17:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Mar 2023 23:17:42 GMT
EXPOSE 27017
# Fri, 31 Mar 2023 23:17:43 GMT
USER 1001
# Fri, 31 Mar 2023 23:17:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:41733b29f9a8eca496b29d689caae2300f16590d79b84a98ea73605fb00ed04b`  
		Last Modified: Fri, 31 Mar 2023 22:29:52 GMT  
		Size: 88.4 MB (88437312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965db94433fcad950bb3fe4287355aa4ff2ca2959240177f242b1563b6a112a4`  
		Last Modified: Fri, 31 Mar 2023 23:20:24 GMT  
		Size: 3.8 MB (3764100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9df441c2425f909bf9f18d2ab72a9c70f164b754c4e542ffc2f4f6b5c40f09e`  
		Last Modified: Fri, 31 Mar 2023 23:20:34 GMT  
		Size: 96.9 MB (96889307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688cabe87b31c3f95cf8b547eb578a9f335268842e148d6c8d170af6833e938a`  
		Last Modified: Fri, 31 Mar 2023 23:20:22 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15930f834c0262bf207dfe3ea5763a52c7b652975993e0719c519e6771dc3791`  
		Last Modified: Fri, 31 Mar 2023 23:20:22 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76131f784fbd596b8db5bd14081a53e04d57876572248adf077efe8f14f7132`  
		Last Modified: Fri, 31 Mar 2023 23:20:20 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62febc3d7b7fe1302dc5a413a57be68b139d7b2cb870c249348f621054db5d07`  
		Last Modified: Fri, 31 Mar 2023 23:20:21 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b3698b855cbea86bca4f476a28b6075036e1166deab27a7e7a59767093fa82`  
		Last Modified: Fri, 31 Mar 2023 23:20:22 GMT  
		Size: 8.1 MB (8137893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c66cf96d3477aed194b91881af25813638ed16300b3d98fd479012d6609d0`  
		Last Modified: Fri, 31 Mar 2023 23:20:20 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1bc63dd4680124845dc722719f77613c4957b96e05c480f8bfc765d84ff685`  
		Last Modified: Fri, 31 Mar 2023 23:20:20 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
