## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:8602d7663c1d8a3acf879f66be73bb30d06b5b4340e60a0c4004131300504bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:dec2545d5094fd66ad70b0af80cd73792a636af71cab7fb9f7ba007b0f7b6ef5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198679258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae142306a4183ed78ed0649dd3d217d0bd7efb320bb32eb6990e157d3bd0af2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 16 Jun 2023 00:20:34 GMT
ADD file:b035aa3f69efa59a3ead304859506efd235c8b26e9ce7e22ad9517c89cc50193 in / 
# Fri, 16 Jun 2023 00:20:35 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:45:42 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 16 Jun 2023 00:46:43 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Fri, 16 Jun 2023 00:46:43 GMT
ENV PSMDB_VERSION=4.4.15-15
# Fri, 16 Jun 2023 00:46:43 GMT
ENV OS_VER=el8
# Fri, 16 Jun 2023 00:46:43 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Fri, 16 Jun 2023 00:46:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 16 Jun 2023 00:47:24 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 16 Jun 2023 00:47:25 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 16 Jun 2023 00:47:25 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 16 Jun 2023 00:47:26 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 16 Jun 2023 00:47:26 GMT
ENV GOSU_VERSION=1.11
# Fri, 16 Jun 2023 00:47:29 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 16 Jun 2023 00:47:30 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 16 Jun 2023 00:47:30 GMT
VOLUME [/data/db]
# Fri, 16 Jun 2023 00:47:31 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 16 Jun 2023 00:47:31 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 16 Jun 2023 00:47:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 Jun 2023 00:47:31 GMT
EXPOSE 27017
# Fri, 16 Jun 2023 00:47:31 GMT
USER 1001
# Fri, 16 Jun 2023 00:47:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d8b19403054493df93762a526e131edad57824e606eb5e37c358828e405ecea1`  
		Last Modified: Fri, 16 Jun 2023 00:22:00 GMT  
		Size: 88.9 MB (88875549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6055b22338fe2f5b4a6e98d2d076ebaf0beec67b7356c94467a33d11d7f2f94d`  
		Last Modified: Fri, 16 Jun 2023 00:50:27 GMT  
		Size: 3.8 MB (3793808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a73130671de07c01c2aa6a0b4e89263939ea429a0d80e5f61157780417a6f1`  
		Last Modified: Fri, 16 Jun 2023 00:50:38 GMT  
		Size: 96.9 MB (96923850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f921b55508a11234576b70c8ec0d598f045d1beb88ce3ff7e5c23eaa6cc0ed`  
		Last Modified: Fri, 16 Jun 2023 00:50:26 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa54213ce41e9b003af24d72b642e457cd9f071608fd88f20b3dd63445be5c`  
		Last Modified: Fri, 16 Jun 2023 00:50:26 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a4af56c96b3dc9c3413fb075c36c3c000fd752870044f672a8abad5aa8767a`  
		Last Modified: Fri, 16 Jun 2023 00:50:24 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32617ce86f98b6c78ed35d718e33442604ae88aec8fc820da85f158112e219a9`  
		Last Modified: Fri, 16 Jun 2023 00:50:24 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cb621c638fe152d12693cebf96dd6e48c0a4a6c94671c191815ce660c98481`  
		Last Modified: Fri, 16 Jun 2023 00:50:25 GMT  
		Size: 8.1 MB (8137891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669e3c405c0865fd1f76ae1704b33ea1f5bb88ef347c3a82f610d3db896815b3`  
		Last Modified: Fri, 16 Jun 2023 00:50:24 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e88355657a07e0d7b2e73ad2d58c43dbadd827445fc1b1f02ad7de22964697`  
		Last Modified: Fri, 16 Jun 2023 00:50:24 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
