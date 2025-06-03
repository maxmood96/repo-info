## `clojure:temurin-24-tools-deps-trixie`

```console
$ docker pull clojure@sha256:ab1c77f838265701a59507332861b75aa95b572d58da140b9613a62c9a3d793a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:df974931567d64687714eddc576530e80c9c13b00ee2a8bf55e1e0a05981c761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227407204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1abf954a1bacdf71728f8c5ffb09c69d47e02e540a572aebc85da2f911b130`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed5b66a39fcecb66ab65669e6f8e5983e9f9744f1d78b32907a229a25b38cbe`  
		Last Modified: Tue, 03 Jun 2025 18:25:09 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4434c8bf63fcf6c2f8ab0cf068195b32bf62fa8c94b99dc3235a6a60f1e9cd3b`  
		Last Modified: Tue, 03 Jun 2025 18:25:11 GMT  
		Size: 88.2 MB (88207252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397b5e561d94f0cb61c50d73c0e1b342490ad172a3e61a4b40e57596a0a0df5f`  
		Last Modified: Tue, 03 Jun 2025 18:24:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7023ab0472d7d3b7aa9098ab18dde36da2ccdad24467d23d608906651d1eb590`  
		Last Modified: Tue, 03 Jun 2025 18:24:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:459d3fb03e1f0e3116d8c916734588ec5fd7fb6e83b11b2d476b416cd90d6299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7284852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cacb9a0eca161cfb1be41289a35876d6acf1ab2fac28b0d95bddac7fd61ec3`

```dockerfile
```

-	Layers:
	-	`sha256:a5088fbcf5de01ecc3d61039fb964d6aee42bd4a336e1740217a842d6e3af9b3`  
		Last Modified: Tue, 03 Jun 2025 21:43:39 GMT  
		Size: 7.3 MB (7269062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be2e4424f8ffe374f50c22f860deac76e7eb8fbd24156ea68d284e27510cad3`  
		Last Modified: Tue, 03 Jun 2025 21:43:39 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:761dafff12b5d0066cdb74baa9ef748a1c7240245bfb179cd458badfcb77bfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227222020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f6a71657c9e556520d8638a577669e19221b995f5738c5e22c5fd91c386ad5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7537e79c58dbcab2941c040399879be549690329edde2c0c79c2f4b2c6e312`  
		Last Modified: Tue, 03 Jun 2025 11:09:31 GMT  
		Size: 89.1 MB (89091276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5992bcac608c256185634db95ff665aa2e77a224954c43f068c6f789fcc31ee`  
		Last Modified: Tue, 03 Jun 2025 18:56:33 GMT  
		Size: 88.5 MB (88511409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d406d0d347e53de391cb59e0275309470cb533383c99422888740c660ce6d96b`  
		Last Modified: Tue, 03 Jun 2025 18:56:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f790d51ad256b8feeaf678efcdd2aa2da81653dfc7bec383f052dea854054359`  
		Last Modified: Tue, 03 Jun 2025 18:56:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3764ebddca29863cec2caa50a8e968cab744c5ec6a25061074ffd7ccb5789d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7291997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe70437d6e318bec413121f449fbafae8b98c6a87034a075a2596a3b8c74c92`

```dockerfile
```

-	Layers:
	-	`sha256:48a460b07dc8613f5ad81761b7fa39b4645c96da7b190bb0b9aacf35562456b0`  
		Last Modified: Tue, 03 Jun 2025 21:43:45 GMT  
		Size: 7.3 MB (7276089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4800657f20562301639825cb8a5643ccda25c9f17d8e5b13cb72957f078d9cd`  
		Last Modified: Tue, 03 Jun 2025 21:43:46 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2ad30fe44f2e3977c65f8a3df59c9ac206832286298a7f951b72ff849b390723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.0 MB (236952115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ccb48c730412a5f4e001e937c1c352b209c63ee28c448144bc69cfa5672c4b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c028c654d0d6c94a628c2a045c90b55cd6b595adae6af5e957fc42510e1de16`  
		Last Modified: Tue, 03 Jun 2025 09:30:35 GMT  
		Size: 89.9 MB (89920265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ed9fb58def414d6264f1202f66b03a9567bee859efbbec8e408fedbf4ab245`  
		Last Modified: Tue, 03 Jun 2025 19:17:02 GMT  
		Size: 94.0 MB (93950265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42d3fcbbac751fdfa6934946c10e0d985fe0a90a7c808b30e33b9ec4500cf8b`  
		Last Modified: Tue, 03 Jun 2025 19:17:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4686b3f9f5abd2195e5f1ec07c95e9f82102b59f970a6b2b1c65db2977e74df`  
		Last Modified: Tue, 03 Jun 2025 19:17:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:52bffd19e8faddfc35bacbef7005489a8b30d1e975d85f6b51f8f4e2f57152f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7290615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837e1d3f12f36a3f32c72bf400a7e6f20c7f3fdae970b0bb2f5ccf48ed61d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:ba1ee9a0e1845becdd6e9a2fcec00689eb909436a0ce91f900b1ed4ed0bdd1eb`  
		Last Modified: Tue, 03 Jun 2025 21:43:52 GMT  
		Size: 7.3 MB (7274777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37c0f45dc51816ecad462fe5fd9e305a020a328dd3bd47e2955a406c3b75d7a`  
		Last Modified: Tue, 03 Jun 2025 21:43:53 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:c8492701a4efbba7ee53aaaaf64f35ba005404eb1a4322710408097ce531c98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222210270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a57c16a67a9cdbeba213281d324e7de720a7556ae2aa029771659d6d87ebf76`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e82597a02bb37801e52c801a502f6b2db3f51568e2ab5f847a48db7ffef1519`  
		Last Modified: Tue, 03 Jun 2025 10:22:55 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cda75bb6e3692d74e80313bbbfec4ddf327a3cb66959329d33039e4ef7b919e`  
		Last Modified: Tue, 03 Jun 2025 19:23:11 GMT  
		Size: 86.9 MB (86855651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f2d56fe1b00ab90da964a098714814a97bea54912a2c54dedc7883c92c792b`  
		Last Modified: Tue, 03 Jun 2025 19:23:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bd0766977d91940da8e7dcd203289def205b8baa6acf1e813ee24bf02fc90e`  
		Last Modified: Tue, 03 Jun 2025 19:23:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c973997876fdc7c046803768bf519c638d9354dd7dfbaae0c2dacc1274c6707d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7272808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4f1739c339773570a72b6bc765da82d827826a6945413074c33b353a932a8b`

```dockerfile
```

-	Layers:
	-	`sha256:b0ccd118c8ae78bb4ae6dfc94d6ee8c3f29aa17c5617224d8caba6078b781fae`  
		Last Modified: Tue, 03 Jun 2025 21:43:59 GMT  
		Size: 7.3 MB (7256970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68606f5fe58f601530c46df53fa8515c0eea0a4f577a889e550901d24da94beb`  
		Last Modified: Tue, 03 Jun 2025 21:43:59 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:065daaebe388d0c68aa9c24650f4e7286a3c2c8eea96a6c6f76537065887c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223493333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40c323f356272d347a9fb1f9290756e8ef47769e8c7d5a0eed1afdbc8f0bbd4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d2065613a1620d7fd64270b68c955b617708425a53d56a91b8997efdf6f3fb`  
		Last Modified: Tue, 03 Jun 2025 06:38:49 GMT  
		Size: 85.2 MB (85216756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff81393802d4050995bf256fdb296e88dc54efd5e5023cd7c188bcc809d9c14`  
		Last Modified: Tue, 03 Jun 2025 18:46:56 GMT  
		Size: 89.0 MB (88953309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24089314f37b9291cea56777960f6cd8a7632ab794ecc530c11e690b27522ec`  
		Last Modified: Tue, 03 Jun 2025 18:46:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10fa2202eb49325f0466ee37b30faf2ee86bfb6a127188ced3f2ce94d20aa07`  
		Last Modified: Tue, 03 Jun 2025 18:46:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a1e8e32385085ddbb1a0eb703a068d523f8d858e21803b928c98ba57aee9accf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7283322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e912010e754811acb444396c76d5b7df840b0925dbc5bc509bf763258734f338`

```dockerfile
```

-	Layers:
	-	`sha256:b74f9cc44513f4114aa0354f839e9afef7367847f4be0cfc02fe3414925237e0`  
		Last Modified: Tue, 03 Jun 2025 21:44:07 GMT  
		Size: 7.3 MB (7267532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d38b75f8eb1568e5c25d0e20ea48b15c55f758193947efb3e37b4bfa0bcdd1b7`  
		Last Modified: Tue, 03 Jun 2025 21:44:08 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
