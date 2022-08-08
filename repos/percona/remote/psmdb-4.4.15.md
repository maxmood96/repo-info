## `percona:psmdb-4.4.15`

```console
$ docker pull percona@sha256:063c3e7b472e76c643275d83e16e3e50d8eea81c85065da48fadc3729bde1b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.15` - linux; amd64

```console
$ docker pull percona@sha256:699e7fc8a09ab741493c7b417289c9e8ad1eb1d0cc7e08f804937452cde7ccae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194618942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881143344407415883579db28b397162b64950c3c9bfd4c068f6feebdac61bdb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 08 Aug 2022 19:40:38 GMT
ADD file:583550feec070b3b62d68508a750a70d39b5f2741fbe7e82268da27c0e92f311 in / 
# Mon, 08 Aug 2022 19:40:39 GMT
CMD ["/bin/bash"]
# Mon, 08 Aug 2022 19:43:44 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Mon, 08 Aug 2022 19:46:25 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Mon, 08 Aug 2022 19:46:25 GMT
ENV PSMDB_VERSION=4.4.15-15
# Mon, 08 Aug 2022 19:46:25 GMT
ENV OS_VER=el8
# Mon, 08 Aug 2022 19:46:25 GMT
ENV FULL_PERCONA_VERSION=4.4.15-15.el8
# Mon, 08 Aug 2022 19:46:25 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Mon, 08 Aug 2022 19:47:02 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Mon, 08 Aug 2022 19:47:03 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Mon, 08 Aug 2022 19:47:03 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Mon, 08 Aug 2022 19:47:04 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Mon, 08 Aug 2022 19:47:04 GMT
ENV GOSU_VERSION=1.11
# Mon, 08 Aug 2022 19:47:07 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Mon, 08 Aug 2022 19:47:08 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Mon, 08 Aug 2022 19:47:09 GMT
VOLUME [/data/db]
# Mon, 08 Aug 2022 19:47:09 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Mon, 08 Aug 2022 19:47:10 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Mon, 08 Aug 2022 19:47:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Aug 2022 19:47:10 GMT
EXPOSE 27017
# Mon, 08 Aug 2022 19:47:10 GMT
USER 1001
# Mon, 08 Aug 2022 19:47:10 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c6c66e8d29aad4dd795924af44e2653db9c88e70d8d5ffc158e799eef5984c4f`  
		Last Modified: Mon, 08 Aug 2022 19:41:30 GMT  
		Size: 84.9 MB (84885626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fdcd871120a4bda85be399a19b14e562689260fc5d1e2ae03c88a622ae48f7`  
		Last Modified: Mon, 08 Aug 2022 19:50:19 GMT  
		Size: 3.8 MB (3757654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27ae4c452fd8aa87d62bfedb98ad5976d370c395f28c073096fd5e6fbfe78c`  
		Last Modified: Mon, 08 Aug 2022 19:50:31 GMT  
		Size: 96.9 MB (96889610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ab2fda6cc0aeefcee2ea65fb32db85f7638e4f1a77a06bda6d160ba0ecd9fe`  
		Last Modified: Mon, 08 Aug 2022 19:50:18 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b4748ff594cadb92da58c3052c1328c91002339cb1d3f4bcd0c10e02d61d46`  
		Last Modified: Mon, 08 Aug 2022 19:50:18 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89451265b0e5cfeeed8c33bfefec0532d4cf37b4d00d347607d08480be6eb903`  
		Last Modified: Mon, 08 Aug 2022 19:50:16 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fea916498c53038037ffd921e595e1e8eb3df92dd1db9b2e770e5165b762908`  
		Last Modified: Mon, 08 Aug 2022 19:50:16 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501faf247c0f456e32215cd33267bae4d7373643570bb6479f6b9ea80a438494`  
		Last Modified: Mon, 08 Aug 2022 19:50:17 GMT  
		Size: 8.1 MB (8137892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65cbcf70541d62244edd2daade7a24c910f85afd94720552160d81eeae1aaa`  
		Last Modified: Mon, 08 Aug 2022 19:50:16 GMT  
		Size: 13.2 KB (13205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4837651e87d68ec632d3861c6ca5c761b3f78a19705ef9e88ca4c06a09fea98`  
		Last Modified: Mon, 08 Aug 2022 19:50:16 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
