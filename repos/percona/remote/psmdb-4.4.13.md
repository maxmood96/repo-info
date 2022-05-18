## `percona:psmdb-4.4.13`

```console
$ docker pull percona@sha256:d8850992a925bcd4999354dbfa8f7271543d49e1014ae7f94bf72654a337bb93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.13` - linux; amd64

```console
$ docker pull percona@sha256:a7662f57aea770b7d731a9cbd68414517717f33f5defd39a2b67a32e2a0ffc71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195488423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f689f00fdc04a8c33b6d6c3b33a95210c1ec0a21784838080d53374c4f9ccc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 17 May 2022 22:41:30 GMT
ADD file:eafd9e49bc2d45c1c5bf5571be43743e0500886224b81c0a07dc7c3d1702d7bb in / 
# Tue, 17 May 2022 22:41:30 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:13:01 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Tue, 17 May 2022 23:15:42 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-44 release
# Tue, 17 May 2022 23:15:42 GMT
ENV PSMDB_VERSION=4.4.13-13
# Tue, 17 May 2022 23:15:43 GMT
ENV OS_VER=el8
# Tue, 17 May 2022 23:15:43 GMT
ENV FULL_PERCONA_VERSION=4.4.13-13.el8
# Tue, 17 May 2022 23:15:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Tue, 17 May 2022 23:16:23 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Tue, 17 May 2022 23:16:24 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Tue, 17 May 2022 23:16:24 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Tue, 17 May 2022 23:16:25 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Tue, 17 May 2022 23:16:25 GMT
ENV GOSU_VERSION=1.11
# Tue, 17 May 2022 23:16:28 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Tue, 17 May 2022 23:16:31 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Tue, 17 May 2022 23:16:31 GMT
VOLUME [/data/db]
# Tue, 17 May 2022 23:16:32 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Tue, 17 May 2022 23:16:32 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Tue, 17 May 2022 23:16:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 May 2022 23:16:32 GMT
EXPOSE 27017
# Tue, 17 May 2022 23:16:32 GMT
USER 1001
# Tue, 17 May 2022 23:16:32 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:25cd53f41add30fe2e87a488316e4bcfbecf123077c0f9f29be5cd359cbafd32`  
		Last Modified: Tue, 17 May 2022 22:42:23 GMT  
		Size: 84.6 MB (84569034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567ff356bca7e3699843c422b64d36df3c5db896eaf92983e8a442cb24e3b3c4`  
		Last Modified: Tue, 17 May 2022 23:19:46 GMT  
		Size: 3.7 MB (3745460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e54ab23a40a5d3b34c5456bc5e723751e3efe5519269c261858b7cd87ed034e`  
		Last Modified: Tue, 17 May 2022 23:19:57 GMT  
		Size: 98.1 MB (98087880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04eb890aea6c167880d481198b5114cfa323964c2752236dd969eb82a4d42308`  
		Last Modified: Tue, 17 May 2022 23:19:45 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fe895677bb450ecd6a3e960c212239f183e02457acf3c7808ff50a3f2e701e`  
		Last Modified: Tue, 17 May 2022 23:19:45 GMT  
		Size: 4.1 KB (4103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c507a79970b040a1e27966f474aaeb553c69a5cdbf01a13ccd7790983515825`  
		Last Modified: Tue, 17 May 2022 23:19:42 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784620c5a428c5284af21ce095568cccc93147a56daa21705433d14e8df4eea5`  
		Last Modified: Tue, 17 May 2022 23:19:43 GMT  
		Size: 914.5 KB (914547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f44d4e570f594422029e58adf2f02884748ded64447f2319924a35d16562f81`  
		Last Modified: Tue, 17 May 2022 23:19:44 GMT  
		Size: 8.1 MB (8137893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8226ce25fdf23286348100186f5d52735846cc131afa365913c027dff6bc2eb`  
		Last Modified: Tue, 17 May 2022 23:19:42 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0ec5cd08e30c8285baddb484f1af0c03c82c71b04b6c2e877d2495419b3cc6`  
		Last Modified: Tue, 17 May 2022 23:19:43 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
