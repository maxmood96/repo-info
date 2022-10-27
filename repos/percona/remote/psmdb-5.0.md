## `percona:psmdb-5.0`

```console
$ docker pull percona@sha256:1c0cf8976a764e40d50cdeac4504f12158c8f7f9ee5dfa87bc09918b2769ab94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-5.0` - linux; amd64

```console
$ docker pull percona@sha256:90dad8a5589181483fc60bd6214b7a9cea8a04fe0aa4b9f82cfab6bac156d501
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211125453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7176c9f951f60fe37caa12fd866e999fa2bf48216da5c4d9c5eaf968e03ba5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 27 Oct 2022 17:21:34 GMT
ADD file:21d51ed5d75272951d93bd7d363ccf19173ef416b25c6acb627b575293fb7389 in / 
# Thu, 27 Oct 2022 17:21:35 GMT
CMD ["/bin/bash"]
# Thu, 27 Oct 2022 17:45:30 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 27 Oct 2022 17:47:01 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-50 release
# Thu, 27 Oct 2022 17:47:02 GMT
ENV PSMDB_VERSION=5.0.10-9
# Thu, 27 Oct 2022 17:47:02 GMT
ENV OS_VER=el8
# Thu, 27 Oct 2022 17:47:02 GMT
ENV FULL_PERCONA_VERSION=5.0.10-9.el8
# Thu, 27 Oct 2022 17:47:02 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 27 Oct 2022 17:47:41 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         procps-ng         jq         tar         oniguruma         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-50/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 27 Oct 2022 17:47:42 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 27 Oct 2022 17:47:43 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 27 Oct 2022 17:47:43 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 27 Oct 2022 17:47:43 GMT
ENV GOSU_VERSION=1.11
# Thu, 27 Oct 2022 17:47:47 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 27 Oct 2022 17:47:51 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 27 Oct 2022 17:47:51 GMT
VOLUME [/data/db]
# Thu, 27 Oct 2022 17:47:52 GMT
RUN set -ex;     curl -fSL https://cdnjs.cloudflare.com/ajax/libs/js-yaml/4.1.0/js-yaml.min.js -o /js-yaml.js;     echo "45dc3dd03dc07a06705a2c2989b8c7f709013f04bd5386e3279d4e447f07ebd7  /js-yaml.js" | sha256sum -c -
# Thu, 27 Oct 2022 17:47:52 GMT
COPY file:e6e9d8018241e8459aecdafe395233cbfaee0351829ed9f41c721972a859a6d6 in /entrypoint.sh 
# Thu, 27 Oct 2022 17:47:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 17:47:52 GMT
EXPOSE 27017
# Thu, 27 Oct 2022 17:47:52 GMT
USER 1001
# Thu, 27 Oct 2022 17:47:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1ca7c848b9e5e4ce2ec73f5399f2b0c161b4c592c979bfb25cd1acc15ea0d84a`  
		Last Modified: Thu, 27 Oct 2022 17:23:09 GMT  
		Size: 86.0 MB (85963514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff15c176357040b466902fc879d5c7c42cb6e78f44aa9857d57a65cb04c300a`  
		Last Modified: Thu, 27 Oct 2022 17:51:37 GMT  
		Size: 3.8 MB (3773708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dc23875a2095f7ee96de4a375d4eeb926539d78b39107896a0d81650543a10`  
		Last Modified: Thu, 27 Oct 2022 17:51:50 GMT  
		Size: 112.3 MB (112302178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b56405d7e1eb861a651e364fc5514a6e9ea940c6ab670bf8fb7e7dd3af00f`  
		Last Modified: Thu, 27 Oct 2022 17:51:36 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b702ec619555688edc0fba8225081fe81871072a6dfc1d47ee6c4d51267ea29c`  
		Last Modified: Thu, 27 Oct 2022 17:51:35 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d3f6ae8747511f4c3f363e6e5beffad0b9296c037ccd5beb5bca25ad39fa36`  
		Last Modified: Thu, 27 Oct 2022 17:51:33 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757d774133b7c19b634dcab01acfa191e6791ac9d5782bee1d7990076d3e7dc8`  
		Last Modified: Thu, 27 Oct 2022 17:51:34 GMT  
		Size: 914.6 KB (914551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabe4f5c45a763523bd2a6757c3a8ce8cb263c225f25fa54ccf77919ecea70eb`  
		Last Modified: Thu, 27 Oct 2022 17:51:35 GMT  
		Size: 8.1 MB (8137892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3893ee9ddf97c359ad8675c0c4a6801e5703b0c2ca49e56929fb167dcf9d8a`  
		Last Modified: Thu, 27 Oct 2022 17:51:33 GMT  
		Size: 13.2 KB (13204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ceed7f0310569a4728287056410f50188b5c4190c3ff30ea106ab88633079a7`  
		Last Modified: Thu, 27 Oct 2022 17:51:33 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
