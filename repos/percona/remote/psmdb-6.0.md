## `percona:psmdb-6.0`

```console
$ docker pull percona@sha256:2c17da21041eaa6db6502ca09d20c0bf1a5b883eb7beee7bb32feace2eb025a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0` - linux; amd64

```console
$ docker pull percona@sha256:3d33e689e759b14ac0a5311ecfa3aa1199804ca9b2ff2a0a57da129aee3a1c39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272720869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c9abd907c76d0580cda6ba351756bf900981024ade2577fca92820ad463456`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:11 GMT
ADD file:20328ed0a20bc722c0afa950a4a513f0ef4fa3ad03131f6e528216ca04acd43f in / 
# Fri, 20 Oct 2023 18:27:11 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:48:25 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 20 Oct 2023 18:49:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 20 Oct 2023 18:49:54 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 20 Oct 2023 18:49:54 GMT
ENV OS_VER=el8
# Fri, 20 Oct 2023 18:49:54 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 20 Oct 2023 18:49:54 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 20 Oct 2023 18:49:54 GMT
ENV PSMDB_REPO=release
# Fri, 20 Oct 2023 18:50:52 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 20 Oct 2023 18:50:54 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 20 Oct 2023 18:50:54 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 20 Oct 2023 18:50:54 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 20 Oct 2023 18:50:54 GMT
ENV GOSU_VERSION=1.11
# Fri, 20 Oct 2023 18:50:58 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 20 Oct 2023 18:51:01 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 20 Oct 2023 18:51:01 GMT
VOLUME [/data/db]
# Fri, 20 Oct 2023 18:51:02 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 20 Oct 2023 18:51:02 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 20 Oct 2023 18:51:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 20 Oct 2023 18:51:02 GMT
EXPOSE 27017
# Fri, 20 Oct 2023 18:51:02 GMT
USER 1001
# Fri, 20 Oct 2023 18:51:02 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f6e7836c36ebb9c4c1c0489873213274f518e7e764c10bf18b60fda601c8dc40`  
		Last Modified: Fri, 20 Oct 2023 18:28:41 GMT  
		Size: 88.0 MB (88003510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0fe297be2aecc89679b1cd2a34b3e156a5ceb5647404173faeee333a0d2f8`  
		Last Modified: Fri, 20 Oct 2023 18:57:03 GMT  
		Size: 3.8 MB (3797309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee6cf1d770291d43a5eb143e2f090d5af63cad0af98e166a7f85bd8334bad19`  
		Last Modified: Fri, 20 Oct 2023 18:57:21 GMT  
		Size: 171.8 MB (171833487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b944b5db72b60ab4ab1bc3b795d4ff540f36ebf182c9a09bbb080efd4e6964`  
		Last Modified: Fri, 20 Oct 2023 18:57:00 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c844be69bbd9131d529da8130e5432a09df5dd8eedbec2f667caf5fb823ccf95`  
		Last Modified: Fri, 20 Oct 2023 18:57:00 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8678645bfac4c586b67c5daa11858d85aa2c45d261e26f9242e6c83a12b66844`  
		Last Modified: Fri, 20 Oct 2023 18:56:58 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c15daa0f6d6c8f88f6ab0f79f2f0628a0041c1fe4d2d3de162df628301f828e`  
		Last Modified: Fri, 20 Oct 2023 18:56:59 GMT  
		Size: 914.5 KB (914545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b8fbec1e977f341c4b291cfab3a1aaef7364afd23bf5dd9bfad01fa80751a7`  
		Last Modified: Fri, 20 Oct 2023 18:56:59 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6529923280384227121299eabe5064c06d1ba7087bf293fe486758a445e8fe2c`  
		Last Modified: Fri, 20 Oct 2023 18:56:58 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f58b0257aff2f7f4ba0a404508938f088851f06b5fe8eed4e8300b0bbe7f58`  
		Last Modified: Fri, 20 Oct 2023 18:56:58 GMT  
		Size: 4.6 KB (4567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
