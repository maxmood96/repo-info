## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:b10b3ca2ea975f30101abb59934756a2fd58c45f4adab63a3c8c27a8cc6f108e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:650991b93218292f9d7c243b888b6344ac752a52da4d364b911a03570206e577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247431646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37300332d3bbb2bf19d151d2fead8b763c83b5fbc8b6278d9e815c552a1ecc88`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:30:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:30:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:30:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:30:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:30:34 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:30:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:30:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:30:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516a61e3ae97e3dd7caf1643a75e4bca15109f4cec18c1c68cfd7e1574e1ac2`  
		Last Modified: Tue, 04 Nov 2025 04:31:11 GMT  
		Size: 145.7 MB (145658307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d26cdf51de7fe076cda3939c195587c869c6bea1275780d3f9ad2d7577e98e`  
		Last Modified: Tue, 04 Nov 2025 04:31:32 GMT  
		Size: 72.0 MB (71994592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ac8b9e2b5e21c9ede78f26d3efa4215f37868bfadbb1369dc1bf577eb78bfb`  
		Last Modified: Tue, 04 Nov 2025 04:31:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e40b2fd69bc3ad7f4f2411f7e4d343f0d737846f78879cd004902bc16d273060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4850c6173f7fa15666baf08017f6da5a9907011a0a31abe2002f073314ee2a60`

```dockerfile
```

-	Layers:
	-	`sha256:0d1b3f9f374c40c88cbf655bba2972dbbd3f3e69d0cc251cd06efd32c82819b6`  
		Last Modified: Tue, 04 Nov 2025 10:38:20 GMT  
		Size: 5.3 MB (5276308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b493252c3dbcc06f979c4388d4878352bb6ae7fd20e9d1e8bf9604f04518e2`  
		Last Modified: Tue, 04 Nov 2025 10:38:21 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ff2581b8fcebd5cbb02b9b97552532bd7c84dfbc6cabf2f7d6b3a7b0d29bc306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244411935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf939c704669f978ed60057b3853b1b856d79bae483eaca9abb6ac0aca83035c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:44:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:44:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:44:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:44:10 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:44:10 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:44:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:44:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:44:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046dcb6c776623e499bcb90943629992e4f4ef7aba7b9e2cc0736005b21feb8b`  
		Last Modified: Tue, 04 Nov 2025 01:44:50 GMT  
		Size: 142.5 MB (142460599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c793d668e2e2d38b374356dd6527423260844a0b198351861eed766810538043`  
		Last Modified: Tue, 04 Nov 2025 01:45:04 GMT  
		Size: 71.8 MB (71808393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf58c429ae122f8eca8f75899ca7beb84cb3806d227cdf38f29af068df75d44`  
		Last Modified: Tue, 04 Nov 2025 01:44:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b33a61597f529930a1799e88a8a7cf42e9d7931b08e6d6802cd82280e5f34177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de87c0df90bb81a43a77e4846de26b1f341c3cd07548b92565b043fd43ce01e`

```dockerfile
```

-	Layers:
	-	`sha256:529aac0fd020b3fddc87b55909415de6149c0de111296da5f02115ec80e41e83`  
		Last Modified: Tue, 04 Nov 2025 10:38:26 GMT  
		Size: 5.3 MB (5282695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56da3111609d21d1b0cf332fc2bfee6dc686b2beac23facffc461034b2f6556a`  
		Last Modified: Tue, 04 Nov 2025 10:38:26 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c8ec15ba2e577dc5d67798c6cf367420c6fc1486adc36c499ce6f39529c01ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243846747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d73dbdce5ca8a9e153bd4c908a81175ad2b2a24d727e334dea63480eabc6ff3`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c44708395cca5d95349579da4a5a7051abf07cac09f2847a4c03d2174d7761`  
		Last Modified: Tue, 21 Oct 2025 21:54:30 GMT  
		Size: 132.9 MB (132853175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573227c122d11d0feec4c48c1a54e045532afc24e6e01a03da0061237dddc938`  
		Last Modified: Tue, 21 Oct 2025 15:45:41 GMT  
		Size: 77.4 MB (77394410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c972b1c17e6b5903a655302a78b99acd48f60a23d2feafa0e6dac00a14655063`  
		Last Modified: Tue, 21 Oct 2025 15:45:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:608d10e22af0238c94be94a46d763fc5aa37a831824bb6cd320ad416ec6a5c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a964e721cd36915f5e777fc6ec0ba7cb1a2e301e38341087593782e6fff7be6c`

```dockerfile
```

-	Layers:
	-	`sha256:77a012924de6aa3b9adffa827184e8a55f33daa445e2a3f3ae1277abaa22d399`  
		Last Modified: Tue, 21 Oct 2025 18:36:27 GMT  
		Size: 5.3 MB (5280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16dde40c2270c80672c06a12d963cd301fccce3fef0d41300d693c49ddfa44bf`  
		Last Modified: Tue, 21 Oct 2025 18:36:28 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f37fcbf882715c2facc51355e678ed282b2cea2d2b4d1a94cfe247df23870861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228413612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23336efc7b59dd5ca34bb00ba5d03b3a1c80eadec60397f826a21a7a8ebe83d`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d1c30d785193c6f831b6cdb06c3747688397a7052d792c3fe37e22083261f9`  
		Last Modified: Tue, 21 Oct 2025 21:49:45 GMT  
		Size: 125.6 MB (125622145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215d801ada748a1a5c573165a0abea34d2acdb73da9e497dbc27c08585752a14`  
		Last Modified: Tue, 21 Oct 2025 22:01:22 GMT  
		Size: 73.0 MB (72953570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd100e80238d3b752d1479c4cdc8724d02ce5820c7169a6e2a6571cb2e3dad03`  
		Last Modified: Tue, 21 Oct 2025 22:01:15 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd5f50d807cf20b9a99423bfafaecf45a6b340d798ea3fa18e38d89674c15511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8019444c68aa14fdc113f2d0bcb1d43d846f40d5ed3ed6a232479c5f0dd51a`

```dockerfile
```

-	Layers:
	-	`sha256:d4e983f06a1f8637e6b4ba3a29efc6c9315b8274c8fc6646531e5aebd93010fa`  
		Last Modified: Wed, 22 Oct 2025 00:36:28 GMT  
		Size: 5.3 MB (5272236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1246091095fade2b1abdf5fabe374fe1f8c8267fa08b747646cd9004292ead50`  
		Last Modified: Wed, 22 Oct 2025 00:36:29 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
