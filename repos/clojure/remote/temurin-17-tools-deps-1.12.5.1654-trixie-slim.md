## `clojure:temurin-17-tools-deps-1.12.5.1654-trixie-slim`

```console
$ docker pull clojure@sha256:412fa2ee9c7a63b597330e4b3896626f8e7a65011e0b746f30100cdb99067181
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

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d3dfdc38b479c3475e6da6bdbfdfa7797587fa72f8dcd749d4cb5e5cbc163b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244643605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325811c687bc8ba3538b21ff7723baf9a3116f878408f04c30504b6e3805a63b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:18:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:18:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:18:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:18:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:18:54 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:19:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:19:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:19:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e168006c86baf8642a975f0d2481ef69002d0993fb16f6f13dd6d07ac2585d`  
		Last Modified: Wed, 24 Jun 2026 02:19:34 GMT  
		Size: 145.9 MB (145905407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54784ddcc0c00e2ef71cab337a74f676295ed4d737934fce4319277fb2a81d7`  
		Last Modified: Wed, 24 Jun 2026 02:19:31 GMT  
		Size: 69.0 MB (68951736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6373bdf9e57fc36fa338975ec397988385b5744538de152aa9e84a5d4f7c08fc`  
		Last Modified: Wed, 24 Jun 2026 02:19:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4f04c4ed8ba33aed10ec3a43520ef67ff5aa226203ed0746496c721ea31407`  
		Last Modified: Wed, 24 Jun 2026 02:19:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8cf0e8304f14d22a233a935b4d01e0d730c6ad5b590a5d8c2ad45c14a3b0715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b112c7de774a71dead81478ba3b1e29cddf5de797452b139b37ed5674dc5447d`

```dockerfile
```

-	Layers:
	-	`sha256:d720be7998d2845c3f99533f8c205b17c2a119cb3c36ff881b9fc18b35f278f9`  
		Last Modified: Wed, 24 Jun 2026 02:19:28 GMT  
		Size: 5.3 MB (5257242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9849d4775b3b39433a7086f5ecf06f43d206683316b054e34917fc0d2bee0c32`  
		Last Modified: Wed, 24 Jun 2026 02:19:27 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8388987bd991fd8b5a830205d068cfa2a99df1599d4359fec7874443ba291c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243651287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8674a61320d21c3c0f86cd942303ee11d4df8fae601bcae07479e5b59a9792`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:25:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:25:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:25:06 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:25:06 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:25:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:25:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:25:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:25:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:25:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82995f2931f959282797570b8ade253ba6513fbe7b456708096121ee1a214dea`  
		Last Modified: Wed, 24 Jun 2026 02:25:45 GMT  
		Size: 144.7 MB (144724309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e537e7718825fbf0021b7cf8856a248dbdee50cd08ce0f63215dde943f0dfb66`  
		Last Modified: Wed, 24 Jun 2026 02:25:44 GMT  
		Size: 68.8 MB (68777391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65f1317b59975dd0a5e66d899bcb290ae6d859a288d087863ed2283a61bf3ae`  
		Last Modified: Wed, 24 Jun 2026 02:25:41 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38ac5f49bbc9685e4d2d19a503f3a523e9345569ac59b7a777cb4a7e4d5dea3`  
		Last Modified: Wed, 24 Jun 2026 02:25:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47b39fb59c22b842fe33fc57af81fecf141167b587adfc25bf6b7199ffb9d582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467e57e7284b43ec39bbe833eec638d9e91742dba1d681bf6926a8e3d3ec8de8`

```dockerfile
```

-	Layers:
	-	`sha256:bccf2c178943962925b87e95d5d6a46add09ab1cd060764d8b9db59bb87073a0`  
		Last Modified: Wed, 24 Jun 2026 02:25:41 GMT  
		Size: 5.3 MB (5263003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f15b06670a854a4b5d83777bc35b302eca75c24fa70c7804192fe04afac55d9`  
		Last Modified: Wed, 24 Jun 2026 02:25:41 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:102d2910f7f2d58e29353283e2243a952c877e92dfd51b468bd270442d953936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253742819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5854224957b51cad7625c025ee8929fc828b7b71cdfcdda1bef84d459c74afc3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:40:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:40:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:40:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:40:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:40:59 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:47:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:47:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:47:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c12061528e7da232c3a05c00802e8fb865782cca2399322852ad4b4c6566c13`  
		Last Modified: Fri, 19 Jun 2026 02:44:54 GMT  
		Size: 145.8 MB (145766192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f41d7200086d79ffc5d53147e5067e72f556db3cc37776a657ce4650915fd7`  
		Last Modified: Fri, 19 Jun 2026 02:48:36 GMT  
		Size: 74.4 MB (74369244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c6996b2f1a4c7cf7c206b6bf835e49a7566a1fb24ec9270476f75a6d78aa64`  
		Last Modified: Fri, 19 Jun 2026 02:48:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224ef0475f26ff21c6084392e5d865636c3af1b26ffb5f4734d93ec7b64dcaf9`  
		Last Modified: Fri, 19 Jun 2026 02:48:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d4b425df88f7ade5b17f17ededed00698d2154d7ecac95eb47bdc3c62ed25be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7db6066c6904f4ead1f06bc567074ebb2faf7e8c9f234c045188fb8c3db64d3`

```dockerfile
```

-	Layers:
	-	`sha256:bf51882d0da10e948527eebcc6d6e83a06bb7c1563bc89ccd1f9bfadae654ba0`  
		Last Modified: Fri, 19 Jun 2026 02:48:33 GMT  
		Size: 5.3 MB (5261613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9525766feb3d13176353a3f5d530c5f445ad02bacf465ec202b88cb8bfa4eb83`  
		Last Modified: Fri, 19 Jun 2026 02:48:33 GMT  
		Size: 16.0 KB (16014 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f522a862f3fed0faf3c61dc0f8c80d075238bca0339f4f9af67de6217c084d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235694624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fab23e8719ab3e31cb58659fb1c6ca66c6d162e179a4673b4f62205de100da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:17:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:15 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:15 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd16adea10fbf1d54ca2e5edb1f4b081332ccd028cf6b0964ac17b7ace1cf74`  
		Last Modified: Fri, 19 Jun 2026 02:18:57 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c83e4129a24958a7e117bc489e1660c125ee9ac508ba45ff3df2c1dc59eb412`  
		Last Modified: Fri, 19 Jun 2026 02:19:50 GMT  
		Size: 69.9 MB (69931805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103f731d874cf0dfece90cb363d7fb093af871a5b87a2f2ddd3657edf3e97b63`  
		Last Modified: Fri, 19 Jun 2026 02:19:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133ef3c43774860444e2150b54f225680e32c4e5e6cbe16841801cc4decd7c70`  
		Last Modified: Fri, 19 Jun 2026 02:19:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa42361061cf6340aa7990c505589794b43979cbc99dfa3500da898f9f1a4968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5f0f7d76c3cbcb53539930d4a5bdad6937cfee644c92f2b7eea66b0599b347`

```dockerfile
```

-	Layers:
	-	`sha256:c270b5694dcf75a59e1dea070d52962a68c78862c9697d68a1ca7adf26fe5f96`  
		Last Modified: Fri, 19 Jun 2026 02:19:49 GMT  
		Size: 5.3 MB (5253166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848b06e238c96eb0abaa5a42d15dc769c7b6a17de55fa5f27cd32a5050d9d52d`  
		Last Modified: Fri, 19 Jun 2026 02:19:49 GMT  
		Size: 16.0 KB (15965 bytes)  
		MIME: application/vnd.in-toto+json
