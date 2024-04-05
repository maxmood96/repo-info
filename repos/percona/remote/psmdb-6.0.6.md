## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:7ee35c22a4f74094efc8a1014783775aea7a0f878a83cc6cf309eb7bb7163fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:c2fb8ef4602ef2957640cb4e695028b0faa76b8735897be208a279176fca1b07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286582022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5989663c1e0a04b170ed9632f2a329cfea68264d2f172e351ec726fbae49fdb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:47:12 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:47:12 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 05 Apr 2024 19:47:12 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:47:12 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 05 Apr 2024 19:47:12 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:47:12 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:48:10 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:48:12 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:48:12 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:48:12 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:48:12 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:48:16 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:48:18 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:48:18 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:48:19 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 05 Apr 2024 19:48:19 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 05 Apr 2024 19:48:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:48:19 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:48:19 GMT
USER 1001
# Fri, 05 Apr 2024 19:48:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681deda51ba9b192c0df38e4b48df88b961befda6254f7dc86acc7b88255b2f8`  
		Last Modified: Fri, 05 Apr 2024 19:53:12 GMT  
		Size: 4.3 MB (4288115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d57d6b900a2e3a585db270fcac060ff18db5bb94a6c938929afbf6fbc8bfb10`  
		Last Modified: Fri, 05 Apr 2024 19:53:31 GMT  
		Size: 172.4 MB (172410341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9963581396707030b08191494a0cd99c207fbd7d74590d38d2c1ffd6c79300eb`  
		Last Modified: Fri, 05 Apr 2024 19:53:10 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0ca7a3502a73fc6a9ad02214e7862ed3484a5891272781c294ec4bb7eac607`  
		Last Modified: Fri, 05 Apr 2024 19:53:10 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc684023ab7b463fa333d090d63fc6ce1712c2543c739dc0bacbebac2633ccb8`  
		Last Modified: Fri, 05 Apr 2024 19:53:08 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3414366b648845db803a466b87071b3ffb88dc75790d5eab673b874c06b343c`  
		Last Modified: Fri, 05 Apr 2024 19:53:09 GMT  
		Size: 914.5 KB (914546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3871d1502b7043994f20a5131576ef297a05343a7133be13d1ee433ee8e0b`  
		Last Modified: Fri, 05 Apr 2024 19:53:10 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d4f1a856538f872e9ec92a01afc05d852385b6bc9016a32bba014c04d39254`  
		Last Modified: Fri, 05 Apr 2024 19:53:08 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2fa33e5ccc4ab803503963ad17beaf34eb4d24bda17f7354ca339337c21dde`  
		Last Modified: Fri, 05 Apr 2024 19:53:08 GMT  
		Size: 4.6 KB (4565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
