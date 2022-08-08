## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:4df6716aa07aef870be3a867d2ef4aa333dac07466c15cafcf54d9ce9f05ae60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:05f68542efaebcca2e576c8fe300fcfae2ce2d26ffd974f04955b0d4605bcd9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.3 MB (175306029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171e3980863cb2746d6201204d3338d4015d0e78e92138a4b66df6d322c7f6e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 08 Aug 2022 19:40:38 GMT
ADD file:583550feec070b3b62d68508a750a70d39b5f2741fbe7e82268da27c0e92f311 in / 
# Mon, 08 Aug 2022 19:40:39 GMT
CMD ["/bin/bash"]
# Mon, 08 Aug 2022 19:43:44 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 08 Aug 2022 19:47:20 GMT
ENV PSMDB_VERSION=4.2.21-21
# Mon, 08 Aug 2022 19:47:20 GMT
ENV OS_VER=el8
# Mon, 08 Aug 2022 19:47:20 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Mon, 08 Aug 2022 19:47:20 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 08 Aug 2022 19:47:23 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Mon, 08 Aug 2022 19:47:58 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Mon, 08 Aug 2022 19:47:59 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Mon, 08 Aug 2022 19:47:59 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Mon, 08 Aug 2022 19:48:00 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Mon, 08 Aug 2022 19:48:00 GMT
ENV GOSU_VERSION=1.11
# Mon, 08 Aug 2022 19:48:03 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Mon, 08 Aug 2022 19:48:04 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Mon, 08 Aug 2022 19:48:04 GMT
VOLUME [/data/db]
# Mon, 08 Aug 2022 19:48:04 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Mon, 08 Aug 2022 19:48:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Aug 2022 19:48:05 GMT
EXPOSE 27017
# Mon, 08 Aug 2022 19:48:05 GMT
USER 1001
# Mon, 08 Aug 2022 19:48:05 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c6c66e8d29aad4dd795924af44e2653db9c88e70d8d5ffc158e799eef5984c4f`  
		Last Modified: Mon, 08 Aug 2022 19:41:30 GMT  
		Size: 84.9 MB (84885626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb06a484521516529f61c86520c62f2e6a492234c50afaeab1b82f16cb8784`  
		Last Modified: Mon, 08 Aug 2022 19:50:44 GMT  
		Size: 3.8 MB (3757712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953f6256b1c0db73576eab17fa6a31124915b20da3e44195e2b12d99b46d7afa`  
		Last Modified: Mon, 08 Aug 2022 19:50:53 GMT  
		Size: 77.6 MB (77589845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e294c3762d655b59ef5f649afc93b423e195d5ee9feb070544dde7384ae87d3e`  
		Last Modified: Mon, 08 Aug 2022 19:50:43 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d880c9db4c0489c6050c88298f35a5a6a87061e1d934412bd94c54d00cf866f`  
		Last Modified: Mon, 08 Aug 2022 19:50:41 GMT  
		Size: 4.1 KB (4097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a04a31d51a40683098818ca05172af8335c6006a0854d36548804971c215a`  
		Last Modified: Mon, 08 Aug 2022 19:50:41 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0387dbeebbf482d66ab4acc2a8fc2559e3481af9e7b8f2fed3775f2abc74dbb1`  
		Last Modified: Mon, 08 Aug 2022 19:50:41 GMT  
		Size: 914.6 KB (914553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458be491c42caac152eb536eb83b70c0be4f1fc8cdeab3dcc5d901d5734011ec`  
		Last Modified: Mon, 08 Aug 2022 19:50:42 GMT  
		Size: 8.1 MB (8137893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7429f1d58a893e7dfb8738005e7b703e3f6b77f36c9353cbb08858e03d40494`  
		Last Modified: Mon, 08 Aug 2022 19:50:41 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
