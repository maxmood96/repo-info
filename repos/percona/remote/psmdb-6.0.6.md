## `percona:psmdb-6.0.6`

```console
$ docker pull percona@sha256:dfcff956c1450b989317e7f3c51a528688d012d9273d6a02f27945b9981befc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-6.0.6` - linux; amd64

```console
$ docker pull percona@sha256:8d16ac171b620f61410200cf4eed57846a7486a9c87a095b5236957f7069ccc2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273742672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfefc22388b8949ae9a0ebfa8e8255a7a16e978a1bf108cf9be61d9c15dd2a31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Aug 2023 01:20:25 GMT
ADD file:66403f2373aff52b265870ad9a159168d6b13e468b8b6f042430bdcc0f1f1d49 in / 
# Fri, 11 Aug 2023 01:20:26 GMT
CMD ["/bin/bash"]
# Fri, 11 Aug 2023 01:43:10 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 11 Aug 2023 01:44:39 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 11 Aug 2023 01:44:39 GMT
ENV PSMDB_VERSION=6.0.6-5
# Fri, 11 Aug 2023 01:44:39 GMT
ENV OS_VER=el8
# Fri, 11 Aug 2023 01:44:39 GMT
ENV FULL_PERCONA_VERSION=6.0.6-5.el8
# Fri, 11 Aug 2023 01:44:39 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 11 Aug 2023 01:44:40 GMT
ENV PSMDB_REPO=release
# Fri, 11 Aug 2023 01:45:31 GMT
RUN set -ex;     percona-release enable psmdb-60 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         percona-mongodb-mongosh         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-60/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 11 Aug 2023 01:45:33 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 11 Aug 2023 01:45:33 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 11 Aug 2023 01:45:33 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 11 Aug 2023 01:45:33 GMT
ENV GOSU_VERSION=1.11
# Fri, 11 Aug 2023 01:45:37 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 11 Aug 2023 01:45:39 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 11 Aug 2023 01:45:39 GMT
VOLUME [/data/db]
# Fri, 11 Aug 2023 01:45:40 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 11 Aug 2023 01:45:40 GMT
COPY file:7ab35f422fd362616b84e1dc71329cc9be05b7f834182c48bf98ceb92ee28956 in /entrypoint.sh 
# Fri, 11 Aug 2023 01:45:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Aug 2023 01:45:41 GMT
EXPOSE 27017
# Fri, 11 Aug 2023 01:45:41 GMT
USER 1001
# Fri, 11 Aug 2023 01:45:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ad03542990defb96a4ce5bef5a0f2f4aa7794d282719d329c9700f8fd2fc4c0`  
		Last Modified: Fri, 11 Aug 2023 01:21:43 GMT  
		Size: 88.9 MB (88922436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0c45cdbc96586817c8b7bc5b4bd8858798f2d665457878d8f9ba40c3cef93c`  
		Last Modified: Fri, 11 Aug 2023 01:51:12 GMT  
		Size: 3.8 MB (3797128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804851dbab35ec8344fc34c03d1ed6514e1b03945b74193e356f87550a0f5013`  
		Last Modified: Fri, 11 Aug 2023 01:51:31 GMT  
		Size: 171.9 MB (171936546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7664eccc64979a403b0f2ffb852c00e5959dbcb02f071283b209aae88849efd8`  
		Last Modified: Fri, 11 Aug 2023 01:51:11 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32785fd05d2c50a1da9ef78831c599820e5d6680389e068708d509fc88845a4b`  
		Last Modified: Fri, 11 Aug 2023 01:51:11 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cbc7f9fed5d8353bd9bddf82c8ba30f1a1a7c38995d5d85ac42044195ed074`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 10.6 KB (10575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4856fb23a26853ef42fb2026eb3f8f12883e231d589b7df1cf971199103874ba`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c4c78d76ceb7228bb9a35c33597bc17a356504fdf0295885dbbd88ae1994df`  
		Last Modified: Fri, 11 Aug 2023 01:51:10 GMT  
		Size: 8.1 MB (8137888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff920c65353a72b414fca77bbe736404060ceac1b85f4b4b0098adbc5a16a1e5`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af1523329e53a1f92910fb6f7044ede1f3859ecc668a9bbc38aa39ad01f6649`  
		Last Modified: Fri, 11 Aug 2023 01:51:09 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
