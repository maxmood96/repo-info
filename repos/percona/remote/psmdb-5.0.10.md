## `percona:psmdb-5.0.10`

```console
$ docker pull percona@sha256:c97e15338185fab521d7a219b5631650fb90e9b8ba80ef7fdc3867175407b467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0.10` - linux; amd64

```console
$ docker pull percona@sha256:1410c28de6f5658818a22c27251037b013ad0390a5ab880cf522af052c0ca1ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214072038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289b1f47108681e5b2b41b0d4c656edc8a393c8da77383452df123056b392598`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 16 Jun 2023 00:20:34 GMT
ADD file:b035aa3f69efa59a3ead304859506efd235c8b26e9ce7e22ad9517c89cc50193 in / 
# Fri, 16 Jun 2023 00:20:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:45:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 16 Jun 2023 00:45:44 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Fri, 16 Jun 2023 00:45:45 GMT
ENV PSMDB_VERSION=5.0.10-9
# Fri, 16 Jun 2023 00:45:45 GMT
ENV OS_VER=el8
# Fri, 16 Jun 2023 00:45:45 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Fri, 16 Jun 2023 00:45:45 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 16 Jun 2023 00:46:27 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 16 Jun 2023 00:46:28 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 16 Jun 2023 00:46:28 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 16 Jun 2023 00:46:29 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 16 Jun 2023 00:46:29 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 00:46:32 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 16 Jun 2023 00:46:35 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 16 Jun 2023 00:46:35 GMT
VOLUME [/data/db]
# Fri, 16 Jun 2023 00:46:35 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 16 Jun 2023 00:46:35 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Fri, 16 Jun 2023 00:46:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Jun 2023 00:46:36 GMT
EXPOSE 27017
# Fri, 16 Jun 2023 00:46:36 GMT
USER 1001
# Fri, 16 Jun 2023 00:46:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d8b19403054493df93762a526e131edad57824e606eb5e37c358828e405ecea1`  
		Last Modified: Fri, 16 Jun 2023 00:22:00 GMT  
		Size: 88.9 MB (88875549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c808133edde960d4d0947bc4f92833e136cd8ebc4b874f44718393224178173`  
		Last Modified: Fri, 16 Jun 2023 00:50:04 GMT  
		Size: 3.8 MB (3793796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacc2ab2a421210ae9f0fa100293c2faf71b5e7497d777ef48e70f25d3040b76`  
		Last Modified: Fri, 16 Jun 2023 00:50:15 GMT  
		Size: 112.3 MB (112316633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452ca793af580d85711cc3e1c9f1a83126c3b9cea818640d7c6b6027d643ead5`  
		Last Modified: Fri, 16 Jun 2023 00:50:02 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851740174399605431af4da5fe8414063766f0d9cea59de27b71131f9f690dcc`  
		Last Modified: Fri, 16 Jun 2023 00:50:02 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ab1c6ad08c28f03081400b68860084be26061827249372761a13e612219b3`  
		Last Modified: Fri, 16 Jun 2023 00:50:00 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4943214938b18270785392d39053a942aeca91035ae7e8999256f8f3fa6f154`  
		Last Modified: Fri, 16 Jun 2023 00:50:01 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1171db59f4b8de8a0cfa92c7e12677f1964984bd714bbedf490dc4bd15c096f`  
		Last Modified: Fri, 16 Jun 2023 00:50:02 GMT  
		Size: 8.1 MB (8137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3daace62bb668df0bbc14047cc8e16e020da68cab41188ca5ef6214d22b4a9e1`  
		Last Modified: Fri, 16 Jun 2023 00:50:00 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4a3e6214281f8e7c8a7e0d8578241f584dab257620bae7394800852ccda678`  
		Last Modified: Fri, 16 Jun 2023 00:50:00 GMT  
		Size: 4.6 KB (4560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
