## `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:55dee9fe001c89295fed4900f655d4164f6b686c164d54f2558a09c69817bbcb
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

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4852799afb55c1f8462a68c3d5500691de4fa047f19a139f6cf7eca8e9962323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219196058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baed87c59c08fc28f1419ba39de2ff80dd2e93911020507d3a7c5c1b58cfb8aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:10 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1822e6fd6c4ec6fe4656df66e41d36b4c1bd3537c94de68ad84e75793f5098`  
		Last Modified: Thu, 04 Jun 2026 17:41:07 GMT  
		Size: 92.6 MB (92574588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b949a4e4fc1d726b961e1df9716f698c368e0889a095dd85a7bf3d3695e333b`  
		Last Modified: Thu, 04 Jun 2026 17:47:33 GMT  
		Size: 78.1 MB (78124999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e1a6942541b77d32a62e18d35059f39b1da9b858e27dcbe29de893c5ea27f9`  
		Last Modified: Thu, 04 Jun 2026 17:47:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0267df897a0feddfbca23b0354a003b35b169a95f0275c31c2de38abc5baf88`  
		Last Modified: Thu, 04 Jun 2026 17:47:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0d65d15d95f11de1e1ce9ce6fb67a090ac6da6c23a115165ad95a9864166771c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6236856bf72ad73e88fd0842f7c956e9feaf31af578b9f33ecbc94f404890a`

```dockerfile
```

-	Layers:
	-	`sha256:10c98798f083cdea2efd70e82e0d70244fe68cc0e193fcf8e9970ffba8d62b86`  
		Last Modified: Thu, 04 Jun 2026 17:47:32 GMT  
		Size: 7.3 MB (7345510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:912061004e8201f89f2105032de57b58ab4429f2989be107f0d6811ea459c339`  
		Last Modified: Thu, 04 Jun 2026 17:47:31 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b7f33b867adda1425201f273921c2ca93ab97d02ffea054a0d9c805c43ebfc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218048233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580998d83257ba433d50202c339614081e931cc69fb7cc8a2e0d8d4cce7e61d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:46:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:51 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d73b51ac5ddeda775806236ab4d2e6e7b71cabbb388252ab24aac27603ec84`  
		Last Modified: Thu, 04 Jun 2026 17:47:28 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c9c444bcb92013161e251ba909b892fb052377ebc3e48c5df982f3076d70be`  
		Last Modified: Thu, 04 Jun 2026 17:47:28 GMT  
		Size: 78.1 MB (78125508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae1bae641c7b2177d7ac797cde7973a6401b2f7ba935373dc0284a1eb537cfc`  
		Last Modified: Thu, 04 Jun 2026 17:47:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae08b1ad1bb7f70619175755ab9f7874ef81f1f7c8a529c3683d26bc1a07c29`  
		Last Modified: Thu, 04 Jun 2026 17:47:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f333ac0b7837dc01a3bc8eac363580b3f6f8fec855196b8f1690725371b1058d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdd81250dbd2acdd4ce21ca7bbebf3ac642643ad8f66338494d51068212cbda`

```dockerfile
```

-	Layers:
	-	`sha256:e965e35e630ffb0f7d9b57c8e3e66491199fe8ef5748c6ddd807903478eabf89`  
		Last Modified: Thu, 04 Jun 2026 17:47:25 GMT  
		Size: 7.4 MB (7351342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0a3caac5ba2e55a212a2dbd53a83df9b35c5d1c311afa6c55ddb6ff0b6092b`  
		Last Modified: Thu, 04 Jun 2026 17:47:25 GMT  
		Size: 18.1 KB (18115 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:973d2bcb9a394bc0443eb62976a1311099d48ed9a3d6a2e0a297a83d4ccdf79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228214314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52508e0f77abc7d2abb941129c622ac6d354e6e983fae09887de450acb241e83`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:22 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:05:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:05:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:05:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:05:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:05:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765ad15186d8d84e420a575b6c5b5cc83f858814242800a49d0e2c53649e1ea9`  
		Last Modified: Thu, 04 Jun 2026 17:42:36 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e43fd4dd30d4e779d0ed6f5328e906a761731f7d384063f8db16d5f3e57724`  
		Last Modified: Thu, 04 Jun 2026 18:06:03 GMT  
		Size: 84.0 MB (83959061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095f77c7294016ce18a955f0108b559f8958165121a4dc6a92e45e6546bf9cb3`  
		Last Modified: Thu, 04 Jun 2026 18:06:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c56125b5ea7a0e3264ff7afde0ca3e0869b919d1f09bcd4d8270f21d917513`  
		Last Modified: Thu, 04 Jun 2026 18:06:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:04987a1d3cae7d247e5d8d56a7c4e467a112c0eae5e849f8509a8d3f11df30ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531ce8cecba93a7d737fe2e57e045948eb14080187d7b78dd5502214165dcaca`

```dockerfile
```

-	Layers:
	-	`sha256:d6c2061e022a1148f8fd978842cfc2cdb0851f518a3175d828b4a9b50ff3c5f0`  
		Last Modified: Thu, 04 Jun 2026 18:06:01 GMT  
		Size: 7.3 MB (7334074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9715fc52650598fb634e4c88a6918f7a1d053fe35769378ddde5f4fa93d040ed`  
		Last Modified: Thu, 04 Jun 2026 18:06:00 GMT  
		Size: 17.1 KB (17056 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:3545a8f827a7201607257cbab20f42ed65bf463ec435d9e57861e496cda8bac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212503319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bce6061428b8d6e75f1802511ea8a544a3ee5ac4e0b6110e7d7e00d6a9717af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:12 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:12 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:45:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd6fd4e1317fe04bcd8332ae62b5c4e80dc94c46ef5970f3958e748fe391485`  
		Last Modified: Thu, 04 Jun 2026 17:45:59 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1f5a5f58115d24e46631cdc6197a2814cfe451ec49074bf8f5c647cac3fe03`  
		Last Modified: Thu, 04 Jun 2026 17:45:59 GMT  
		Size: 76.9 MB (76926365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a571e8063bc08492ea80588c7e78a6a5bf69439559e3f19f8fb26916bdfc73`  
		Last Modified: Thu, 04 Jun 2026 17:45:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b4fc75eb28e49b0636928a894196b37214e32381b7121474f90a15fb0ed360`  
		Last Modified: Thu, 04 Jun 2026 17:45:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0c4f5090d1df13db86177cf45b83038b5f9415f31166daba64e8f5dc5e592b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f3b3441db2b7cdd416cc06bbeafc1424158f09e2acc71d9179dd63cb5bc6f6`

```dockerfile
```

-	Layers:
	-	`sha256:53197fa83e84ed403fcc521fc34ee77107139c14c0886eae8956b75570c96be6`  
		Last Modified: Thu, 04 Jun 2026 17:45:56 GMT  
		Size: 7.3 MB (7321391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f50d7014a51a25377f0454be43e2aa412d22cc2e4e333a8b6c1fd92f84b228d0`  
		Last Modified: Thu, 04 Jun 2026 17:45:56 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json
