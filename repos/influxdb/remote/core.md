## `influxdb:core`

```console
$ docker pull influxdb@sha256:31ad94df2248134989b2cf73d965e51dd5f35dfae22d7ed8f4776b12e6f69f4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:2a33df848aa7e3110aa16d53642e9a0049413bc3549800aa30f3524a4cf6604d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149127978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30799fe936a4c3feda6e44ed98270c5f1eb40430c1a340a6675165c646941f58`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:30:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:30:14 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:30:19 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:30:19 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:30:19 GMT
USER influxdb3
# Mon, 04 May 2026 19:30:19 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:30:19 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:30:19 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:30:19 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:30:19 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0150fdeaff076406fcb3a0c4aa18adf46fb2fbb198e2232890493f8fee6c0bd`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 6.7 MB (6672455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d0a189ea13679d8de8790c8207bb78913300cef22bf6c22dca410a226b9f08`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdd7d5e6bee01c1e036187795eda83e4de4724db84c3313152063861e927cb`  
		Last Modified: Mon, 04 May 2026 19:30:40 GMT  
		Size: 112.7 MB (112718222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ebd3cb97923e17f7d330643a76d1b460fe10f7b30af7d2d3c1750cc672975`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede128c13a48993b91017a4040191e412a2b84a1b360f498d6f494a36df1ba2b`  
		Last Modified: Mon, 04 May 2026 19:30:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:49664c981cea3b12231c6dcf35f5b9ea94fcade463b25febf6a944359da3a564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9630edcca1790e79f0afb1d5e18a21fee2f33172c92521ed5cce8c3a110dd`

```dockerfile
```

-	Layers:
	-	`sha256:f55f07cbe1ba319f4fb641561ce3b8c04caaf4e83764e4ca7f9032b649920b88`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09dbe94fe189d04cc2285f2ccff91d7f69338f6afbd7f000e681371e6532bd87`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 17.6 KB (17620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:52d9872ab1e55a055dd3f7b5268f5c6c2b029cb8b68f858c23f0aad0b79831a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140106553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19979a9a1a5887ca0db7a0955919bfef6d9fa32db9c94087e5f504fb83d5af85`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:24:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:24:42 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:24:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:24:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:24:47 GMT
USER influxdb3
# Mon, 04 May 2026 19:24:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:24:47 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:24:47 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:24:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:24:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86122c5ae2f33c5829b37b51c97108e5d0affc9a8df38a2520c2547957be231`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 6.7 MB (6682327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9912325bdc1215b07db51f9c07ae6e8820f419585f5b9887242a1fe13c7613d6`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b125a45984c5269b6fa91084249fabb15107023aa0b6b970da45b12c244f228`  
		Last Modified: Mon, 04 May 2026 19:25:06 GMT  
		Size: 104.5 MB (104544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8864d3ce3dc01bc91806893665a5b7fc0a8b446a18b11dab323970528b26f0c`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba1d612389a4091467addf28fb0d3c3d2403a29bb18848dd001ec6e3e032fb9`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:a18ae06ad6d18c7f881a4b49c8d07d0cb3230600e42b332e69f8de458933da8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e147252f5eea6b419a730b9f59f8f268481a1395aa6b563d14563c918a6d5f8b`

```dockerfile
```

-	Layers:
	-	`sha256:f5e73fadd1e444f21baa13cf65d30006e79055f47e5fdee04f18b8c6941a04a3`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9efa154e53131da2dc68d5b78f59fc7828711e79ff576b57b71b56c777b161c`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 17.8 KB (17768 bytes)  
		MIME: application/vnd.in-toto+json
