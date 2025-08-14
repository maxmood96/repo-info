## `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:17f8e71bcff59701b02ac096c2021aeffe3fc6147df645d2fc54ec1a2f21675a
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:21baed93c2025bab451358787f3d987f7b1179957bf189ffab90aeec0304f1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243423361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4fce158e50af57f643d89e45b78354946f391f9bbe4598ecf9887de0885229`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c854a34bf11cf83289c3803271d493df796662a78cb45674c642ba4fe282da5`  
		Last Modified: Wed, 13 Aug 2025 07:56:54 GMT  
		Size: 145.7 MB (145658173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c537d6572c855c2e75c3722481e2291230f1b8cfeeba42267eb50115b079b1`  
		Last Modified: Tue, 12 Aug 2025 21:36:11 GMT  
		Size: 69.5 MB (69534288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2a31d48b324f4bb48c4c2421adf81e183499a3106a6e69f309388ab553ac79`  
		Last Modified: Tue, 12 Aug 2025 21:36:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a325ba077c857dd993eee7aa078dc08265788284dae7bd1f9c4c974057f02ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b496e3943576c0586e837b679c6ef94d7c149d0550d73a8a7dad3b8950553da5`

```dockerfile
```

-	Layers:
	-	`sha256:9fd691a10619bb58e0bea9e608d828e0bda99a616a0908098a4c437ebb2979a4`  
		Last Modified: Wed, 13 Aug 2025 00:35:13 GMT  
		Size: 5.1 MB (5131385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9259faa7636c3e78c5e40a72573afcc0692fd198ec8aa8ac4a908336c37d8eaa`  
		Last Modified: Wed, 13 Aug 2025 00:35:14 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f0662e61ab96499d45b067bb92f94768cc36d65c49284d310232dc465ca87a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239948155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c211b5ca23cd8091bd43d377a50bf9958516ba339a09995b51ed7b442d8d3dc9`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49dadd71684a8b2cbdcb1cf7c2821ae6d645770a2917b11e72b260500475d47`  
		Last Modified: Thu, 14 Aug 2025 07:28:17 GMT  
		Size: 142.5 MB (142460557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf8ecb92e203feb3da80ecf7c3bc15c54ee024ffed333b5dbd201cb31f4e16e`  
		Last Modified: Wed, 13 Aug 2025 14:17:33 GMT  
		Size: 69.4 MB (69404955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db4fd27d799ca295c4aaeb47d4d0f16c4bd4a2a0aea7350a8bedb6919b1fb97`  
		Last Modified: Wed, 13 Aug 2025 14:17:16 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b24ea76334f574894b7fd14d8dbc2299debafd59066587247be8cd45b113ad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe63c7c621ce39dbd477df6f466996658f4cc60609dd1c9ccbacd51378bd9a7`

```dockerfile
```

-	Layers:
	-	`sha256:b87015b5e6cf49aed78d46ad39412c879136c7bfd22b7fc0391555bdab5a92b7`  
		Last Modified: Wed, 13 Aug 2025 15:35:14 GMT  
		Size: 5.1 MB (5137764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:562441e6b05964fa0f336699a7fef1f798a88d1b1a24cfefadae852537a3f60c`  
		Last Modified: Wed, 13 Aug 2025 15:35:15 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2c2acced756f75e10317720d5e60ac2f90bbb01da8330c58f7d9b13ad004bea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240288748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfdd6cb1758de2e8af9c50084493c1b5ebaa8709cba84d13a9697df7b9b63cc`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7ae0c2378afb3370e8d1fef7bee9cc44ef7b1cfbe4567be112936672ed706d`  
		Last Modified: Wed, 13 Aug 2025 19:33:26 GMT  
		Size: 132.9 MB (132853269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c068c46c4d8290003f7e8e265704a57d2a6c1f1fb867d49be92adacca11baf6c`  
		Last Modified: Wed, 13 Aug 2025 19:40:51 GMT  
		Size: 75.4 MB (75361413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6263a1aca36fef62d42d89704775a9fc3c6346d7efc0cf80157d10e1fd9f48e`  
		Last Modified: Wed, 13 Aug 2025 20:19:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:74974a4a43bc886552d843936c3634829ce53eecb3b9821bcc35746484c601d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ace82235acadd887bdf48d95e91dbbc9d1196f585810177671c23d406812fe1`

```dockerfile
```

-	Layers:
	-	`sha256:bc2dc66e5686199e90ec5aad0bc12f78bda24ef95a29feebf9b2efd852efb708`  
		Last Modified: Wed, 13 Aug 2025 21:35:14 GMT  
		Size: 5.1 MB (5135928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1c6bd2a7f2ec69d8009273b5a7a7fb6260abcda4e2dda61d53c35c3c3f23b3`  
		Last Modified: Wed, 13 Aug 2025 21:35:15 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:099f10ce3183a05fa8878476a393af91e05aa524a5e3551d784c261fe30b81a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220852339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ac3dbb34eae0e046d4a7813e533655defaf94953df42e5806b553164184270`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b861e110ba8e24b59ca45696523f44d29430dffbe3a84561dc7a78bf452dcf`  
		Last Modified: Wed, 13 Aug 2025 19:16:10 GMT  
		Size: 125.6 MB (125622089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d62c1a9b7144401eff98f3dae4c0987356a81368a6c7b87da329680f9772b20`  
		Last Modified: Wed, 13 Aug 2025 18:07:00 GMT  
		Size: 68.3 MB (68341771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6190a94b4c980898999fb6c4c26fdf3f7ebccaf8380b5c530252b4a719424cc8`  
		Last Modified: Wed, 13 Aug 2025 18:16:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4fc3e97ec30c0ff9fa64834036eff262116267f728eb9128f6609b94834f8201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314b33cefc0b1860c25cd05c6ce8f8f175d1aa151a798717491c3aa0ddcd2425`

```dockerfile
```

-	Layers:
	-	`sha256:29577a14bec6ba814335657985bd0b5c9b4ea8137849aea4d71b2f13b321c8df`  
		Last Modified: Wed, 13 Aug 2025 18:34:48 GMT  
		Size: 5.1 MB (5122710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935f95dd960f0699c34d79374cca10538375f5db9beb3a636c15f9f4113215ce`  
		Last Modified: Wed, 13 Aug 2025 18:34:49 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
