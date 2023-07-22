## `percona:psmdb-4.2.24`

```console
$ docker pull percona@sha256:6d037151ba2c77cccb9d4bc46b89bcba9c58e02dc4fc28dcbf5e30e7744bfa94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.24` - linux; amd64

```console
$ docker pull percona@sha256:087d8663bdfe11637535d12b7e960409cabf248ed99a24f28dc251040a915f74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219082302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4c5df10ff5dc98e5623c3fbfdbe9e23feb7519ad0a2a24bedb9eca7968dc16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:23 GMT
ADD file:2845c17548800304aa52d90847926434497a1ef1dda1e2e5f0971c74294ae482 in / 
# Sat, 22 Jul 2023 01:20:23 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:44:57 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Sat, 22 Jul 2023 01:49:53 GMT
ENV PSMDB_VERSION=4.2.24-24
# Sat, 22 Jul 2023 01:49:53 GMT
ENV OS_VER=el8
# Sat, 22 Jul 2023 01:49:53 GMT
ENV FULL_PERCONA_VERSION=4.2.24-24.el8
# Sat, 22 Jul 2023 01:49:53 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Sat, 22 Jul 2023 01:49:53 GMT
ENV PSMDB_REPO=release
# Sat, 22 Jul 2023 01:49:56 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Sat, 22 Jul 2023 01:50:44 GMT
RUN set -ex;     percona-release enable psmdb-42 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Sat, 22 Jul 2023 01:50:45 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Sat, 22 Jul 2023 01:50:45 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Sat, 22 Jul 2023 01:50:45 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Sat, 22 Jul 2023 01:50:45 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Jul 2023 01:50:48 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Sat, 22 Jul 2023 01:50:51 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -;     rm -f /tmp/SHA256SUMS;     chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Sat, 22 Jul 2023 01:50:51 GMT
VOLUME [/data/db]
# Sat, 22 Jul 2023 01:50:51 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Sat, 22 Jul 2023 01:50:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 22 Jul 2023 01:50:51 GMT
EXPOSE 27017
# Sat, 22 Jul 2023 01:50:51 GMT
USER 1001
# Sat, 22 Jul 2023 01:50:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:c606e6160312209a2b40622410bcfab5f08671bdd452d36cfbfc4a8a27d5ef70`  
		Last Modified: Sat, 22 Jul 2023 01:21:30 GMT  
		Size: 88.9 MB (88927012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e59d8262edc3761fc898e9536e1bfd4d42b54084ca172bbe7a069bcfba1038`  
		Last Modified: Sat, 22 Jul 2023 01:53:44 GMT  
		Size: 3.8 MB (3801613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdafea38407c8a9d31b4df88b7a4a835c3ff93c073cdfa0b6c0841f16c367da7`  
		Last Modified: Sat, 22 Jul 2023 01:53:58 GMT  
		Size: 117.3 MB (117266765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f243375913fb722f206536fe7d21f036323e3de7585dd16b36dfdf03c19249`  
		Last Modified: Sat, 22 Jul 2023 01:53:43 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc426d1182cc48c6c89f5d43910971a3f6fcbb8b5ef6b8df1251a1c0974ebb6`  
		Last Modified: Sat, 22 Jul 2023 01:53:41 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d3c1f5a6509565113e9392906b87704e74702877ceffd9a84e9e1077dfcd20`  
		Last Modified: Sat, 22 Jul 2023 01:53:41 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a4f26de695f52cf4f4eebdd15fd211b107c5c0d2658b83b1123ab3fb55c177`  
		Last Modified: Sat, 22 Jul 2023 01:53:42 GMT  
		Size: 914.5 KB (914544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4c6e7f357e0685b71f96235c37fba23de26f53af95f4ce2d5305987b312ce1`  
		Last Modified: Sat, 22 Jul 2023 01:53:43 GMT  
		Size: 8.2 MB (8151453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b828ae934356e274e079c90de0639e81e129e0837564cbac8edd1325d6941e`  
		Last Modified: Sat, 22 Jul 2023 01:53:41 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
