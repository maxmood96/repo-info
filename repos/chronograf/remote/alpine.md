## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:6a13c94781499351f6019fa26d02dc287e361d973bb5e97e58e0a25bba2579d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a9f3b74a26e54cae5a6c7fb7b5e4abf40daa069403992677e6c5dc0753c9bb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62307276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4ba0108a1b6fbb590dc2b7e493f9b3d520846ff0b6a0875264a036e18e7a90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 02 Jun 2026 19:04:41 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Tue, 02 Jun 2026 19:04:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/usr/bin/* &&     cp -a /usr/src/chronograf-*/usr/bin/* /usr/bin &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 02 Jun 2026 19:04:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 02 Jun 2026 19:04:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287062304c09ba75dc0e215866a324ed37b156260de2f4620bb8f91128ab548e`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f12ca20af43c42fcda6630eb29e46ed6428b3442e1c5a3a7058c666c91f74`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 312.2 KB (312201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae5737a7f7c4257e5f9e07b9d767ac92f8fa0cc21a23e84f3353d9c012a0692`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 58.2 MB (58162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f1d07db993877635002f6bf86983ac5552cb29152ca78b3ed8dba4b0f74a8d`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf29867af4e0e03fc4f2fe6a37ef5ce2e757d32aeacc686721a470943fde4ec`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1777423041239cd1143016601133645e295a3bd49e139f0337486cafa72133`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:08db9de38b0153583acd24af21133c549def40c9dec94d56e28a1b7025bab203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3e7acde3366a74927292f173102513f05008301d3188d9dc8e16fd66e5a60f`

```dockerfile
```

-	Layers:
	-	`sha256:efd1fcc3b8aed71cbabb698176ad48290ef7f148a172fec85141612648087af0`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 269.3 KB (269314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845aece1bc937a99c1da8fb155a6937175ad801820bf47a5256b3c43596afc12`  
		Last Modified: Tue, 02 Jun 2026 19:04:57 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json
