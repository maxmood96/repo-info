## `percona:psmdb-4.2.19`

```console
$ docker pull percona@sha256:003a874f42f7e29e7254641204793a1c97ac373640b102584f751e085c1d2b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `percona:psmdb-4.2.19` - linux; amd64

```console
$ docker pull percona@sha256:3b923727402cfcf1b03c76310fcf9c93e436a13e846b0bafae8ad8c771882514
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179086862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26aa61588484bc2ba65ffd42f658f1bb7cded7fe1ff16b3ccff1eab418238e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:33 GMT
ADD file:d94132182c035117e6c34ac6179798583b0adcdb2790160d2740b5a23dfef57b in / 
# Tue, 29 Mar 2022 18:35:34 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:14:40 GMT
LABEL org.opencontainers.image.authors=info@percona.com
# Thu, 31 Mar 2022 02:16:55 GMT
ENV PSMDB_VERSION=4.2.19-19
# Thu, 31 Mar 2022 02:16:55 GMT
ENV OS_VER=el8
# Thu, 31 Mar 2022 02:16:55 GMT
ENV FULL_PERCONA_VERSION=4.2.19-19.el8
# Thu, 31 Mar 2022 02:16:55 GMT
ENV K8S_TOOLS_VERSION=0.5.0
# Thu, 31 Mar 2022 02:16:59 GMT
RUN set -ex;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A 99DB70FAE1D7CE227FB6488205B555B38483C65D 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1;     gpg --batch --export --armor 430BDF5C56E7C94E848EE60C1C4CBDCDCD2EFD2A > ${GNUPGHOME}/RPM-GPG-KEY-Percona;     gpg --batch --export --armor 99DB70FAE1D7CE227FB6488205B555B38483C65D > ${GNUPGHOME}/RPM-GPG-KEY-centosofficial;     gpg --batch --export --armor 94E279EB8D8F25B21810ADF121EA45AB2F86D6A1 > ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     rpmkeys --import ${GNUPGHOME}/RPM-GPG-KEY-Percona ${GNUPGHOME}/RPM-GPG-KEY-centosofficial ${GNUPGHOME}/RPM-GPG-KEY-EPEL-8;     curl -Lf -o /tmp/percona-release.rpm https://repo.percona.com/yum/percona-release-latest.noarch.rpm;     rpmkeys --checksig /tmp/percona-release.rpm;     rpm -i /tmp/percona-release.rpm;     rm -rf "$GNUPGHOME" /tmp/percona-release.rpm;     rpm --import /etc/pki/rpm-gpg/PERCONA-PACKAGING-KEY;     percona-release enable psmdb-42 release
# Thu, 31 Mar 2022 02:17:34 GMT
RUN set -ex;     dnf -y install         percona-server-mongodb-mongos-${FULL_PERCONA_VERSION}         percona-server-mongodb-shell-${FULL_PERCONA_VERSION}         jq         procps-ng         oniguruma         tar         policycoreutils;             curl -Lf -o /tmp/Percona-Server-MongoDB-server.rpm http://repo.percona.com/psmdb-42/yum/release/8/RPMS/x86_64/percona-server-mongodb-server-${FULL_PERCONA_VERSION}.x86_64.rpm;     rpmkeys --checksig /tmp/Percona-Server-MongoDB-server.rpm;     rpm -iv /tmp/Percona-Server-MongoDB-server.rpm --nodeps;     rm -rf /tmp/Percona-Server-MongoDB-server.rpm;     dnf clean all;     rm -rf /var/cache/dnf /var/cache/yum /data/db && mkdir -p /data/db;     chown -R 1001:0 /data/db
# Thu, 31 Mar 2022 02:17:35 GMT
RUN useradd -u 1001 -r -g 0 -s /sbin/nologin             -c "Default Application User" mongodb
# Thu, 31 Mar 2022 02:17:35 GMT
COPY file:b7c621ae843e72f20dd7ef20e8c42b89234688ceed5018592c3e5bfa61048aad in /licenses/LICENSE.Dockerfile 
# Thu, 31 Mar 2022 02:17:36 GMT
RUN cp /usr/share/doc/percona-server-mongodb-server/LICENSE-Community.txt /licenses/LICENSE.Percona-Server-for-MongoDB
# Thu, 31 Mar 2022 02:17:36 GMT
ENV GOSU_VERSION=1.11
# Thu, 31 Mar 2022 02:17:38 GMT
RUN set -eux;     curl -Lf -o /usr/bin/gosu https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64;     curl -Lf -o /usr/bin/gosu.asc https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-amd64.asc;         export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify /usr/bin/gosu.asc /usr/bin/gosu;     rm -rf "$GNUPGHOME" /usr/bin/gosu.asc;         chmod +x /usr/bin/gosu;     curl -f -o /licenses/LICENSE.gosu https://raw.githubusercontent.com/tianon/gosu/${GOSU_VERSION}/LICENSE
# Thu, 31 Mar 2022 02:17:40 GMT
RUN set -ex;     curl -fSL https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/k8s-mongodb-initiator -o /usr/local/bin/k8s-mongodb-initiator;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/mongodb-healthcheck -o /usr/local/bin/mongodb-healthcheck;     curl -fSL  https://github.com/percona/mongodb-orchestration-tools/releases/download/${K8S_TOOLS_VERSION}/SHA256SUMS -o /tmp/SHA256SUMS;     echo "$(grep 'k8s-mongodb-initiator' /tmp/SHA256SUMS | awk '{print $1}')" /usr/local/bin/k8s-mongodb-initiator | sha256sum -c -;     echo "$(grep 'mongodb-healthcheck' /tmp/SHA256SUMS   | awk '{print $1}')" /usr/local/bin/mongodb-healthcheck   | sha256sum -c -;     rm -f /tmp/SHA256SUMS;         chmod 0755 /usr/local/bin/k8s-mongodb-initiator /usr/local/bin/mongodb-healthcheck
# Thu, 31 Mar 2022 02:17:40 GMT
VOLUME [/data/db]
# Thu, 31 Mar 2022 02:17:40 GMT
COPY file:f695d42c4add7cde05638253f593b5a3f599ec240da8e578b8c6049c6e1672a9 in /entrypoint.sh 
# Thu, 31 Mar 2022 02:17:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 31 Mar 2022 02:17:40 GMT
EXPOSE 27017
# Thu, 31 Mar 2022 02:17:40 GMT
USER 1001
# Thu, 31 Mar 2022 02:17:40 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f194d33a6f3eb80ec1d36f30e468274de9bc57c56876707532a364fe1edb59b7`  
		Last Modified: Tue, 29 Mar 2022 18:36:37 GMT  
		Size: 87.5 MB (87480759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a9196a2b63c43733b5b1fd2967ff517b596682f6cfb561839409ce6ae0b3a`  
		Last Modified: Thu, 31 Mar 2022 02:19:48 GMT  
		Size: 3.8 MB (3754358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1f2efe43365bbd63e0b9b5a0542cb2fc5653639c93548a8497ae01430567bf`  
		Last Modified: Thu, 31 Mar 2022 02:19:56 GMT  
		Size: 78.8 MB (78778905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5f4658b6fc0f0aebe991ac64b4602a1798bb643491db4eb7d68bed655ec2e4`  
		Last Modified: Thu, 31 Mar 2022 02:19:47 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3472ac7e48535cc7e1bb61afc5ddac80dfbdad136ceee804d2bbc64c67180090`  
		Last Modified: Thu, 31 Mar 2022 02:19:44 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6b80237edf4bd6238f7ccea3c452e7e6b1a8bf252402f5867839ceaa7e9259`  
		Last Modified: Thu, 31 Mar 2022 02:19:45 GMT  
		Size: 10.6 KB (10579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ddeab79e9a4edf1adb6f85541e55c4280234f591647682b96db007cc2d3e6c`  
		Last Modified: Thu, 31 Mar 2022 02:19:45 GMT  
		Size: 914.5 KB (914550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7467d5e4d72343ed2189b35fd66276e462a485c40fb6b8f86e141ab826167`  
		Last Modified: Thu, 31 Mar 2022 02:19:46 GMT  
		Size: 8.1 MB (8137889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8798a05d9c78e10a77f4bd75e697e3b846fb333becfa511c9e0943b80b66ae`  
		Last Modified: Thu, 31 Mar 2022 02:19:44 GMT  
		Size: 4.6 KB (4556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
