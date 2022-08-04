## `percona:psmdb-4.2.21`

```console
$ docker pull percona@sha256:dd2ca71fc16a7339bf2633d2f732e0e2eef622890e9d8c7f4a709f00138ef173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.21` - linux; amd64

```console
$ docker pull percona@sha256:1eb412094dfda1ae385d4c269c95a03c6e190b4d0cc929f3e787234483d9f49d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176255420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1731cc8a72abec4260c17cbe4dd43e0d942b6daa17d40b06778e1db9e0dbffe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 04 Aug 2022 00:36:24 GMT
ADD file:a5c0188d3e4384a1f788282e3e08114ef4bbdc6c4380027e1bd5bce1bc4e5198 in / 
# Thu, 04 Aug 2022 00:36:25 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 01:27:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 04 Aug 2022 01:30:53 GMT
ENV PSMDB_VERSION=4.2.21-21
# Thu, 04 Aug 2022 01:30:53 GMT
ENV OS_VER=el8
# Thu, 04 Aug 2022 01:30:53 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Thu, 04 Aug 2022 01:30:53 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 04 Aug 2022 01:30:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Thu, 04 Aug 2022 01:31:30 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 04 Aug 2022 01:31:31 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 04 Aug 2022 01:31:32 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 04 Aug 2022 01:31:32 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 04 Aug 2022 01:31:32 GMT
ENV GOSU_VERSION=1.11
# Thu, 04 Aug 2022 01:31:34 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 04 Aug 2022 01:31:36 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 04 Aug 2022 01:31:36 GMT
VOLUME [/data/db]
# Thu, 04 Aug 2022 01:31:36 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Thu, 04 Aug 2022 01:31:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Aug 2022 01:31:36 GMT
EXPOSE 27017
# Thu, 04 Aug 2022 01:31:37 GMT
USER 1001
# Thu, 04 Aug 2022 01:31:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fae47290d1d4680e418ff0e417295a1a662b380f965dde612c1f7602670ffabd`  
		Last Modified: Thu, 04 Aug 2022 00:37:18 GMT  
		Size: 84.6 MB (84583462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f569dcb69a1b51a56a3d06a2ed40120922da15d6e9b8a6783a13fd6c3ef4a`  
		Last Modified: Thu, 04 Aug 2022 01:34:17 GMT  
		Size: 3.7 MB (3747486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a906018fdd7f53e2ff81608403463ca8d855907b3754e10b36f657b21c177a`  
		Last Modified: Thu, 04 Aug 2022 01:34:26 GMT  
		Size: 78.9 MB (78851631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee082e2af4adb7607b414823df7b3a76e5a09df264bed6ef01a2337735d2c3d9`  
		Last Modified: Thu, 04 Aug 2022 01:34:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb70ab61dccc676597a9a7cd78e7389e44e3e85f7ff4f03ad75afd8a87a84ae`  
		Last Modified: Thu, 04 Aug 2022 01:34:14 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b137e2f5d44b684c422e96d2946f1eb286fa8b1323934b095e462046140b403`  
		Last Modified: Thu, 04 Aug 2022 01:34:14 GMT  
		Size: 10.6 KB (10576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3e66d0519705a74b3d660fe2fe1e03e979a997a9bd2f7cbef5d0777e1980bf`  
		Last Modified: Thu, 04 Aug 2022 01:34:14 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2397f8f8dc7602f371120623084d3427df3c52bae7703b73f5932ad4a91415`  
		Last Modified: Thu, 04 Aug 2022 01:34:15 GMT  
		Size: 8.1 MB (8137890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b52400ec8c40fdbccfa7596fa3aeae728329f2b21ec110968212ffd8291dda`  
		Last Modified: Thu, 04 Aug 2022 01:34:14 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
