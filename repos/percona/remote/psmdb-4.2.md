## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:4b02ab29c024a8a3de8dbda2aaa02be459f7bf137975bfb73f74a4d044cf330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:b49cac9506892b5853a80e96479b1d2c2a87f6a68b171c73abf2e42f7c8310bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231963063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749956f05d28366b18c3a78f0db22a8d79d91accc59b7aeecf45ee5b277b2778`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:18 GMT
ADD file:10ca901c24a84f484a66ec1b21b29e715054301d7a2b19b9059dfbc233f31f31 in / 
# Fri, 08 Mar 2024 19:21:19 GMT
CMD ["/bin/bash"]
# Fri, 08 Mar 2024 19:40:04 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 08 Mar 2024 19:45:30 GMT
ENV PSMDB_VERSION=4.2.24-24
# Fri, 08 Mar 2024 19:45:30 GMT
ENV OS_VER=el8
# Fri, 08 Mar 2024 19:45:30 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Fri, 08 Mar 2024 19:45:30 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 08 Mar 2024 19:45:30 GMT
ENV PSMDB_REPO=release
# Fri, 08 Mar 2024 19:45:33 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 08 Mar 2024 19:46:24 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 08 Mar 2024 19:46:25 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 08 Mar 2024 19:46:25 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 08 Mar 2024 19:46:26 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 08 Mar 2024 19:46:26 GMT
ENV GOSU_VERSION=1.11
# Fri, 08 Mar 2024 19:46:29 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 08 Mar 2024 19:46:31 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 08 Mar 2024 19:46:31 GMT
VOLUME [/data/db]
# Fri, 08 Mar 2024 19:46:31 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 08 Mar 2024 19:46:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Mar 2024 19:46:32 GMT
EXPOSE 27017
# Fri, 08 Mar 2024 19:46:32 GMT
USER 1001
# Fri, 08 Mar 2024 19:46:32 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f68bbd02e59af82434daa66d365e994a7b1dce7fe0565cbd35d5bec4a2c210b6`  
		Last Modified: Fri, 08 Mar 2024 19:22:50 GMT  
		Size: 100.8 MB (100799993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d30b856bbfc5b0d02fa88a7c4f2d29c4bef830bff12f467ece789abfdef7c4a`  
		Last Modified: Fri, 08 Mar 2024 19:50:16 GMT  
		Size: 4.3 MB (4304227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d608d01d2a1faaf5a21a940e534c16066095b0d8322f30e7c077357607ceb233`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 117.8 MB (117771915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78034ba415818b29f68a1b3f05ec21c7800f09b15e7297128692f1c5937d4469`  
		Last Modified: Fri, 08 Mar 2024 19:50:15 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41cdbae717278a6b00499d4d5094d0651b94f56bcc5f4b34e33193371b24297`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7bb8c77c2027e35e6f8cef6991baaf4527b27db92bd246a57b222a7b01c465`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ebb89f9b0b8218a3ab5fa29c08d012cab229d4173f4850869f5a532f662626`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86f8d408851cc2a7df3c2a0aee79d843a7742d151e91cdf203892739ba05e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:15 GMT  
		Size: 8.2 MB (8151464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa78d4184def64aa834478252e8a3b11c6774552d09748aadadbbfc0c73a0c7d`  
		Last Modified: Fri, 08 Mar 2024 19:50:13 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
