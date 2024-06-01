## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:14a1ed711ca65747a2fc9e2094f6e5d3dea10a6f71985216ae21379fbec0f8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:c0ddf1348f8afb33051980d8287fac4599aeb6ccad35463c811cda694b22c02b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231808346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f540a18280135f220950c99ce6acf5a9c28f2a77994d46caa57ec58633291ab3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 01 Jun 2024 00:48:21 GMT
ADD file:d0210abd288b830fbfd40531ba3d6494278a57d2c92f3d2ec8809ec7d1b2f3cf in / 
# Sat, 01 Jun 2024 00:48:22 GMT
CMD ["/bin/bash"]
# Sat, 01 Jun 2024 01:38:50 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 01 Jun 2024 01:44:29 GMT
ENV PSMDB_VERSION=4.2.24-24
# Sat, 01 Jun 2024 01:44:29 GMT
ENV OS_VER=el8
# Sat, 01 Jun 2024 01:44:29 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Sat, 01 Jun 2024 01:44:29 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 01 Jun 2024 01:44:29 GMT
ENV PSMDB_REPO=release
# Sat, 01 Jun 2024 01:44:32 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 01 Jun 2024 01:45:26 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 01 Jun 2024 01:45:27 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 01 Jun 2024 01:45:28 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 01 Jun 2024 01:45:28 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 01 Jun 2024 01:45:28 GMT
ENV GOSU_VERSION=1.11
# Sat, 01 Jun 2024 01:45:32 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 01 Jun 2024 01:45:35 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 01 Jun 2024 01:45:36 GMT
VOLUME [/data/db]
# Sat, 01 Jun 2024 01:45:36 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sat, 01 Jun 2024 01:45:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Jun 2024 01:45:36 GMT
EXPOSE 27017
# Sat, 01 Jun 2024 01:45:36 GMT
USER 1001
# Sat, 01 Jun 2024 01:45:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:713134d2a3b753ba8ed0b36fca07bb0d670ba16f3699a0ee0bf96971dc8861c9`  
		Last Modified: Sat, 01 Jun 2024 00:50:30 GMT  
		Size: 100.7 MB (100687170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08437527b413502ca7d129217ebf1c1219980457fa03f229fd38c3eb1f67c4b5`  
		Last Modified: Sat, 01 Jun 2024 01:49:15 GMT  
		Size: 4.3 MB (4284328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3419d86d757489cbad6f23971b617a6abf1d1d067774085bc6b8e2d0f3ea0dd9`  
		Last Modified: Sat, 01 Jun 2024 01:49:29 GMT  
		Size: 117.7 MB (117749999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f975cf23577c288ccdce46292bafdd0ebd2810860d0eca2712011490bc1a2e`  
		Last Modified: Sat, 01 Jun 2024 01:49:14 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da284916143c4c2331757661e94a880164e62b7c473da85ce7991dc3cc9cbf86`  
		Last Modified: Sat, 01 Jun 2024 01:49:12 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a040cd4b8864caee176cfe2476bdec1bfda8349a320202e6540de82de17dcd3c`  
		Last Modified: Sat, 01 Jun 2024 01:49:13 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f17382e814da8c20d3dc2885769937a943a706d3ba03c25b9c7fca903168685`  
		Last Modified: Sat, 01 Jun 2024 01:49:13 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7807a633fb4a2ad0e474d173f2c6a0c8751120a1c4b540354a21348f6091d7`  
		Last Modified: Sat, 01 Jun 2024 01:49:14 GMT  
		Size: 8.2 MB (8151461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6310d236e1102b5de9fdb27fc35a4f42548e5c0f39c3e96b879c9b8d37839d`  
		Last Modified: Sat, 01 Jun 2024 01:49:13 GMT  
		Size: 4.6 KB (4555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
