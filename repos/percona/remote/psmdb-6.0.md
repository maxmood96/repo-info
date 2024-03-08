## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:e1f543ecab041850ce6abebaef13ee5e54b3b493cb11a0abddedab055897525b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:787b3c63909d12c498a94d41e1d92cedd8a68bbb2d2ecce509d66c52de71a9ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286571607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392cdbe58c4136a20fdaa92f39d34b06487b62e4848c4a27b63c67a16f566c73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:41:49 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:41:49 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 08 Mar 2024 19:41:49 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:41:49 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 08 Mar 2024 19:41:49 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:41:49 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:42:46 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:42:47 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:42:47 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:42:48 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:42:48 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:42:52 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:42:55 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:42:55 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:42:55 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 08 Mar 2024 19:42:55 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 08 Mar 2024 19:42:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:42:56 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:42:56 GMT
USER 1001
# Fri, 08 Mar 2024 19:42:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9587e819e22f1da9e25539345bd39f6429f2911cafe6c433bc588563f198089d`  
		Last Modified: Fri, 08 Mar 2024 19:48:47 GMT  
		Size: 4.3 MB (4304196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74645974e5ba1cfc0eed468e337297d603c1a5a6eec3aa16d2fec89c65de9a9f`  
		Last Modified: Fri, 08 Mar 2024 19:49:07 GMT  
		Size: 172.4 MB (172380843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf08b3296571a78e7818cef8db205b81c9cfe8f98765170eed15f0a44142815`  
		Last Modified: Fri, 08 Mar 2024 19:48:46 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfd597b85c2b86d74fb78b9dbfa8dd68fcf69623e35899900a04a3a87819988`  
		Last Modified: Fri, 08 Mar 2024 19:48:46 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda329fea3176232df37cba69c0ea5c6a4b224c9b5ca1393a159959851287ad8`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd31ae03eff8443ce798c7eac79ca7cda175706be5dbe96d7e5c265e4210542a`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a69235949454acb09846f32770926bbcc7c4d4afbe53e45ae18656a4cb66d34`  
		Last Modified: Fri, 08 Mar 2024 19:48:46 GMT  
		Size: 8.1 MB (8137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab93e7a6b7d34b1450edb654540ee4b9645ee18e8a7da88f8c344e6ec677ea95`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39a6acf07b17bdb8963c98ae72a4a70000c886505ad3a8d63f96de53f3563bf`  
		Last Modified: Fri, 08 Mar 2024 19:48:44 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
