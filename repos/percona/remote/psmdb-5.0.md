## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:a8e704007cd22dde4ae34f48b655a2e0ed70415d691eded388d545115888ddb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:c744dc2fd8f47026eb86477fddf95ec405e8f027ca9cad67c8275c2bc484b3b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213629953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b6fd560b403e955991384e0d6aa534e10555bc208788e903b80448f35dd02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Apr 2022 20:32:54 GMT
ADD file:2d97892bf8c2eeadd8df675df73ede6f6bc115c021f3e5c43267a14ad84f678e in / 
# Wed, 27 Apr 2022 20:32:55 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 22:11:09 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Wed, 27 Apr 2022 22:12:28 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Wed, 27 Apr 2022 22:12:28 GMT
ENV PSMDB_VERSION=5.0.7-6
# Wed, 27 Apr 2022 22:12:28 GMT
ENV OS_VER=el8
# Wed, 27 Apr 2022 22:12:29 GMT
ENV FULL_PERCONA_VERSION=5.0.7-6.el8
# Wed, 27 Apr 2022 22:12:29 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Wed, 27 Apr 2022 22:13:08 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Wed, 27 Apr 2022 22:13:09 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Wed, 27 Apr 2022 22:13:09 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Wed, 27 Apr 2022 22:13:10 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Wed, 27 Apr 2022 22:13:10 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Apr 2022 22:13:14 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Wed, 27 Apr 2022 22:13:17 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Wed, 27 Apr 2022 22:13:17 GMT
VOLUME [/data/db]
# Wed, 27 Apr 2022 22:13:18 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Wed, 27 Apr 2022 22:13:18 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Wed, 27 Apr 2022 22:13:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Apr 2022 22:13:18 GMT
EXPOSE 27017
# Wed, 27 Apr 2022 22:13:18 GMT
USER 1001
# Wed, 27 Apr 2022 22:13:18 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:79f01b38ff93019ac23e41c2714bc448edcfdd0a5bc3cc47488aa0544086e2ee`  
		Last Modified: Wed, 27 Apr 2022 20:33:41 GMT  
		Size: 87.5 MB (87481556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36610d2f17c8e98ff7beca8478611b0a7ef33e185cd45bb277b6c09e5f8175d2`  
		Last Modified: Wed, 27 Apr 2022 22:16:47 GMT  
		Size: 3.8 MB (3765226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b901902927cd513bd131f194b2f038c863849194bbbe991b074f7f650f223548`  
		Last Modified: Wed, 27 Apr 2022 22:17:01 GMT  
		Size: 113.3 MB (113297121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de33b4516fb216e133847be61260d9a9e560ddf21852dc105644bfadefb18e2`  
		Last Modified: Wed, 27 Apr 2022 22:16:46 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd78c1a760adb8e9d58aa57e9cfa9c97620420649a61f2e742c57945fffc4569`  
		Last Modified: Wed, 27 Apr 2022 22:16:46 GMT  
		Size: 4.1 KB (4098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e246c63ac1fa5b6530b317983ba6cff856da52816c17eb84d80786be880338d7`  
		Last Modified: Wed, 27 Apr 2022 22:16:44 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d842a9ad74e12e321a4dac7b67d4e9f9839fa08a40464832f5f446bde07a56ef`  
		Last Modified: Wed, 27 Apr 2022 22:16:44 GMT  
		Size: 914.6 KB (914552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296621b3168d1f5da225d0d4f31e339c1740c3b4d2d0f8bcac63ab142e434b27`  
		Last Modified: Wed, 27 Apr 2022 22:16:45 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aecb31ca88b8acd656f8fa58482817050341b4d95303eba6e98b8c770723670`  
		Last Modified: Wed, 27 Apr 2022 22:16:44 GMT  
		Size: 13.2 KB (13206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b460575da28c34b290789f303ccdcc57e73d8710b7d9547add7257f31caaa4`  
		Last Modified: Wed, 27 Apr 2022 22:16:44 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
