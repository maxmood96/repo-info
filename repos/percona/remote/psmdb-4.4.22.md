## `percona:psmdb-4.4.22`

```console
$ docker pull percona@sha256:65b68fd8c09b4c0304b3d7153dcc7ea1694be5e80eb37fe948e75a77ec12bc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.4.22` - linux; amd64

```console
$ docker pull percona@sha256:5d90ec4cb9a5ff479db6f7ae37a653adee5d3d652e7fcbbde8c0278c417a9886
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250456238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50913c5b9b3c2853ad15b363c391405648d73dabe488d2df984045596656f702`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 05 Apr 2024 18:23:27 GMT
ADD file:871a3d7925b6335a9cdab3b4740e84d6a8f20bc1aacc682368f1bfc5735c9afc in / 
# Fri, 05 Apr 2024 18:23:28 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:45:27 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Fri, 05 Apr 2024 19:47:12 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY
# Fri, 05 Apr 2024 19:49:43 GMT
ENV PSMDB_VERSION=4.4.22-21
# Fri, 05 Apr 2024 19:49:43 GMT
ENV OS_VER=el8
# Fri, 05 Apr 2024 19:49:43 GMT
ENV FULL_PERCONA_VERSION=4.4.22-21.el8
# Fri, 05 Apr 2024 19:49:43 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Fri, 05 Apr 2024 19:49:44 GMT
ENV PSMDB_REPO=release
# Fri, 05 Apr 2024 19:50:39 GMT
RUN set -ex;     percona-release enable psmdb-44 ${PSMDB_REPO};     dnf config-manager --enable ol8_u4_security_validation;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         percona-server-mongodb-tools-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         cyrus-sasl-gssapi         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-44/yum/${PSMDB_REPO}/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Fri, 05 Apr 2024 19:50:41 GMT
RUN useradd -u 1001 -r -g 0 -m -s /sbin/nologin             -c "Default Application User" mongodb;     chmod g+rwx /var/log/mongo;     chown :0 /var/log/mongo
# Fri, 05 Apr 2024 19:50:41 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Fri, 05 Apr 2024 19:50:41 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Fri, 05 Apr 2024 19:50:41 GMT
ENV GOSU_VERSION=1.11
# Fri, 05 Apr 2024 19:50:44 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Fri, 05 Apr 2024 19:50:47 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Fri, 05 Apr 2024 19:50:47 GMT
VOLUME [/data/db]
# Fri, 05 Apr 2024 19:50:48 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Fri, 05 Apr 2024 19:50:48 GMT
COPY file:2e691e8e3c29008da8a3c85bbe67de1e1e3fbb73ae7ec22473431d5a771341bf in /entrypoint.sh 
# Fri, 05 Apr 2024 19:50:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:50:48 GMT
EXPOSE 27017
# Fri, 05 Apr 2024 19:50:48 GMT
USER 1001
# Fri, 05 Apr 2024 19:50:48 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a9ec167ae4db010539147b23b98bc8201b63b2b646ed53bc6332a2aa47acc33b`  
		Last Modified: Fri, 05 Apr 2024 18:24:32 GMT  
		Size: 100.8 MB (100797004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681deda51ba9b192c0df38e4b48df88b961befda6254f7dc86acc7b88255b2f8`  
		Last Modified: Fri, 05 Apr 2024 19:53:12 GMT  
		Size: 4.3 MB (4288115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbbe57d18d24736c1d1b3ff6c549e10d6bd9083176765aee196dbad13fa4a8c`  
		Last Modified: Fri, 05 Apr 2024 19:54:29 GMT  
		Size: 136.3 MB (136284563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc0974382b68e21d3c497cdc6498b3bf368b5af6897e3aa0c8eb140a1aa13c4`  
		Last Modified: Fri, 05 Apr 2024 19:54:12 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8844c2b540df45e7d629f89a1e6cb442ff4d578b2f676e4476424cfcfceb5a64`  
		Last Modified: Fri, 05 Apr 2024 19:54:12 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9169e69a2057a8f06a53716519693658a7fcbe718e6d9619aa8d55d5b149001d`  
		Last Modified: Fri, 05 Apr 2024 19:54:10 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9b7de59b007697cb9827a4e350398d3eb8b2476ebeef528c0936930b16bbf1`  
		Last Modified: Fri, 05 Apr 2024 19:54:11 GMT  
		Size: 914.5 KB (914547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65011163cb64940679b0644276e5f8fb1bf2af36d22c914668f166f20721026`  
		Last Modified: Fri, 05 Apr 2024 19:54:11 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71944d9d13a6f3633f70c759812caeee4d3117a09831dae121ebb27c8d93657`  
		Last Modified: Fri, 05 Apr 2024 19:54:10 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904666679d8d9fac9af37bfaf29efb6f9b249557ddfbbfc45061cb3a13829011`  
		Last Modified: Fri, 05 Apr 2024 19:54:10 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
