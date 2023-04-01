## `percona:psmdb-4.2`

```console
$ docker pull percona@sha256:f9ad2964bf056303239f91658936d1af997c61f344e9406da8d4c04174dad332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2` - linux; amd64

```console
$ docker pull percona@sha256:510d04795cc0e07553587a2d3160ebb59ea88f6bc38cfe85173d5100a42300f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178851870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9299a80bf78be8bb798f6dbd577cc365a31d0912c2b03e19755774dc32c4925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 31 Mar 2023 22:28:30 GMT
ADD file:612f06c9f5ab410219b2415de45592033d4e9a8d5ce398134276a90224363fb7 in / 
# Fri, 31 Mar 2023 22:28:31 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:15:56 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 31 Mar 2023 23:17:51 GMT
ENV PSMDB_VERSION=4.2.21-21
# Fri, 31 Mar 2023 23:17:51 GMT
ENV OS_VER=el8
# Fri, 31 Mar 2023 23:17:51 GMT
ENV FULL_PERCONA_VERSION=4.2.21-21.el8
# Fri, 31 Mar 2023 23:17:51 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 31 Mar 2023 23:17:54 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Fri, 31 Mar 2023 23:18:31 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 31 Mar 2023 23:18:32 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Fri, 31 Mar 2023 23:18:32 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 31 Mar 2023 23:18:33 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 31 Mar 2023 23:18:33 GMT
ENV GOSU_VERSION=1.11
# Fri, 31 Mar 2023 23:18:36 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 31 Mar 2023 23:18:37 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 31 Mar 2023 23:18:37 GMT
VOLUME [/data/db]
# Fri, 31 Mar 2023 23:18:37 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Fri, 31 Mar 2023 23:18:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Mar 2023 23:18:38 GMT
EXPOSE 27017
# Fri, 31 Mar 2023 23:18:38 GMT
USER 1001
# Fri, 31 Mar 2023 23:18:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:41733b29f9a8eca496b29d689caae2300f16590d79b84a98ea73605fb00ed04b`  
		Last Modified: Fri, 31 Mar 2023 22:29:52 GMT  
		Size: 88.4 MB (88437312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023d12b40e011da061e752cdaf777e2e447e302bf8168943751eac42162c98ed`  
		Last Modified: Fri, 31 Mar 2023 23:20:45 GMT  
		Size: 3.8 MB (3764143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cca3bd6033d9f6a4249a76ad71b813278ce9e28de0329f4df3b0390a285cce`  
		Last Modified: Fri, 31 Mar 2023 23:20:53 GMT  
		Size: 77.6 MB (77577579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476160d168881ca7608e19d9b3210692f3538283ce82b37050ff8fe80e41dcab`  
		Last Modified: Fri, 31 Mar 2023 23:20:44 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b3b062cb21e65dd6e296df0ee9a8a6acbf4df435a8181b2ad960869fe44939`  
		Last Modified: Fri, 31 Mar 2023 23:20:42 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d397bf9b8fe5867fc937d97a3e2a72cb4685d065e6846b28437d271d8b4027`  
		Last Modified: Fri, 31 Mar 2023 23:20:42 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4513b6620b9fd474b69f050fe420704a1a7f264b14c7b67091c5a268f251af8`  
		Last Modified: Fri, 31 Mar 2023 23:20:43 GMT  
		Size: 914.5 KB (914549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aae029485f0d95e9708445f8aaa4cfff514c51a368c98829732f11270d5557`  
		Last Modified: Fri, 31 Mar 2023 23:20:44 GMT  
		Size: 8.1 MB (8137887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f788ce2eb080448498e6e7490dd5a273b04dbfc9c8a06de723ca626d27f53eb`  
		Last Modified: Fri, 31 Mar 2023 23:20:42 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
