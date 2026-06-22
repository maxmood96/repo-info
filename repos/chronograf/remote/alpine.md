## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:3a4d1bdde45637be9b012855ab2ecf9847c9bca2629e5895ceff0f08525cd1ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:52a00a974fa31ab104f5615656f1f1ba19124d9dae74d1e3e19095da738ba4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62242533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3562034250a9e0cf4501b816388ce00db408d02585ac8df9a5f1c9eef9387bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:11 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 19:56:11 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Mon, 22 Jun 2026 19:56:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/usr/bin/* &&     cp -a /usr/src/chronograf-*/usr/bin/* /usr/bin &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 22 Jun 2026 19:56:16 GMT
VOLUME [/var/lib/chronograf]
# Mon, 22 Jun 2026 19:56:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:16 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5117c3486ea43e29efca00448cabc535b8f239d757c2ea33ef0320285384ab97`  
		Last Modified: Mon, 22 Jun 2026 19:56:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c138ad4109725f9ac144c7b23085967f20ab7006fd27272598882e140227af`  
		Last Modified: Mon, 22 Jun 2026 19:56:23 GMT  
		Size: 268.0 KB (268025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c7d0596ef7237fc88fb03d77af3d61b002a1e42ded225a97f9fc69ee2fe95d`  
		Last Modified: Mon, 22 Jun 2026 19:56:30 GMT  
		Size: 58.2 MB (58162177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881dc26ef020f0cad884e72944ebec73a1f795973e8bfb6c6db1e41060f44516`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0292f8295b205f521c6f751540b266d56de9079017576ebe9221ceff52b54b42`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48ef1b877e834580c226ecf1161f71b15017d2168d2f2546ee3982dd9be936a`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:53d0c74f55399512e8bcbaf8564c4bdef51e154b5945714c13c0cf04a9fd1873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 KB (270191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43529a8845f8039709e8625c631ae8596244bc3cb3a04816f708e98ea86e12e4`

```dockerfile
```

-	Layers:
	-	`sha256:240b9e5d786fcf925327de71a60eb8944708565e23237bec28592aba486cbeee`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 252.4 KB (252427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b290ab107110c261f7aeca24b0147ea4138218fee2d23ddf55b64e55f42ae82c`  
		Last Modified: Mon, 22 Jun 2026 19:56:28 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json
