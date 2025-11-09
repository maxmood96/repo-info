## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:ea6328c81e750b1b4543aa173aa0506e08f8bbc5364af5395c6bbde5eb455723
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:29202e550f10a3ef133aa3a278fec81b6c9026a10647cc7a82f01edc616b3b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152642050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06f8f3be0c9c93b4514a22f4c5c523b1bfffd68cd3e5db2db76b6e801344d14`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:04:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:04:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:04:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:04:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:04:15 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:04:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:04:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:04:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1367c31ef9db53e612b8c7570d5fe1df2fa273628bdf7f24d46dbf932a281ef7`  
		Last Modified: Sat, 08 Nov 2025 18:04:56 GMT  
		Size: 54.7 MB (54733343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be240b36c1aa95c8f4ef853cab8185b071b4039f854831736d50d3ed12eb81e`  
		Last Modified: Sat, 08 Nov 2025 18:05:02 GMT  
		Size: 69.7 MB (69679494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375f603303b839be9682c441dcf0d71f5a19ba8b84852ca9db9a4ee7ea5cf41d`  
		Last Modified: Sat, 08 Nov 2025 18:04:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:94c73c18a837752b18fa8b26db59720b8ddf0a16283d7472f5904d9118995876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d644c3ee981e82915e875da2a3f274cf2ec3c8eb26d570dcaaf18a7dfe6dc4e0`

```dockerfile
```

-	Layers:
	-	`sha256:21aff18f37b3273878e9ec4c7f615db75a90cdcf901d94da56e7184a6b1f3d93`  
		Last Modified: Sat, 08 Nov 2025 19:37:45 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a9fa520328f1079f5c869e5244a5b4f7d85bf6e2a0c13b47514b72a0ba8ee9`  
		Last Modified: Sat, 08 Nov 2025 19:37:46 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2592cbccec0a271846b6d96553aafb0cdff84375913879514c14ce2b9a9a1a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151478373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fb641a1fca3d292432634902b07f47588cd6aa1e660c32c8e23776a22b1131`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:03:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:03:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:03:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:03:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:03:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:03:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:03:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d65e2c645922bca495cc09b41e5fb6607a461cc075f841130727e1fe1abad97`  
		Last Modified: Sat, 08 Nov 2025 18:04:25 GMT  
		Size: 53.8 MB (53815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c141792b1403dd4954790dd63fd1dff278463570ac134b2dbc1165254fe554b`  
		Last Modified: Sat, 08 Nov 2025 18:04:30 GMT  
		Size: 69.6 MB (69560307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d4fe1af67ee63a8b272d93b1ecf297616f54f775d80f18d3a510e875ad1524`  
		Last Modified: Sat, 08 Nov 2025 18:04:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92a83316141d855aef270dd51e8679166d8b04e194e0b5931b9b38be6f552a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ac415cd9f2796792f87eae27cc7889543e23ba974c329e4b0a17cb9dc6a9a3`

```dockerfile
```

-	Layers:
	-	`sha256:f47ee91eac5f38b1591dd8e7c1bf12b5b0ab37b040377836e2ceb727ae307011`  
		Last Modified: Sat, 08 Nov 2025 19:37:53 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4866ad7031878f0dfb4be3805ca508b893234eca71e73ddbeb1eff235f79ac7`  
		Last Modified: Sat, 08 Nov 2025 19:37:53 GMT  
		Size: 14.4 KB (14365 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e26e57f7d7acc0b4a5e62cfde72322273d8c464576340581ed52c169b38063a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159757990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed2d60dfd20e2e9d121835043acafa1b2f526b341ac65af270dc3beabdaa036`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:08:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:08:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:08:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:08:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:08:39 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:16:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:16:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:16:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38274692e792c055b238d8ce9d9c11f70979045035705415d76d4de7efadf57`  
		Last Modified: Sat, 08 Nov 2025 19:10:48 GMT  
		Size: 52.2 MB (52175136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1048598ada8bc0cc69713271769eeaeb0cf675ed03938341459d7b83798d4aa`  
		Last Modified: Sat, 08 Nov 2025 19:19:07 GMT  
		Size: 75.5 MB (75513303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fc3d25835b36008f5735444aa32bca4c3990faea3d2c7d2153ccf98f84d88d`  
		Last Modified: Sat, 08 Nov 2025 19:18:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d96f06a713c867f90a475839827182ac0278d47a7980513852f8191c7319cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bc7c643650b3d265a145eb650dcbc0cfab00501624caa118dc6919af2d60c5`

```dockerfile
```

-	Layers:
	-	`sha256:2506e0663a00079f591fc1fd895eaad270df372e3554853bb457a8bf6e03f6fc`  
		Last Modified: Sat, 08 Nov 2025 22:54:12 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c104d5a0dd8dd2a12f46af013ee004ee3faca8e393a19e599fcc61cf1575ee2`  
		Last Modified: Sat, 08 Nov 2025 22:54:13 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.in-toto+json
