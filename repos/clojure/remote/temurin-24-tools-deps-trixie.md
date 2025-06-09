## `clojure:temurin-24-tools-deps-trixie`

```console
$ docker pull clojure@sha256:28a6c4d0cb25b91079c742b5d3d756c38e64dab826fff5c5935fc0f9758f57b5
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
$ docker pull clojure@sha256:370547cfcf1ede9c80795f5199802531fe44677c8042905a925a2b71309c22e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227406605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd5f1ea2200ee267513a0ae844612674ea2486dcbdca94c368e10d60f1e2474`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca8130b01352467a2ae4563900dc69157eb0e08a50ec3d6fd6f3709b99e4feb`  
		Last Modified: Mon, 09 Jun 2025 17:19:37 GMT  
		Size: 90.0 MB (89951996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81afbd51f467babee0500e9ba761ffaced1edab50d9192847ee8406e980883cd`  
		Last Modified: Mon, 09 Jun 2025 17:19:37 GMT  
		Size: 88.2 MB (88206660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1f6104780873b0c284e824e3aec11bec89219e98c3d295cd1b1e31a76d9b84`  
		Last Modified: Mon, 09 Jun 2025 17:19:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e59bc4b56d1a37e4e9599b276c60838db2eb2f6959fcc8b0f5a53db98abe2`  
		Last Modified: Mon, 09 Jun 2025 17:19:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4357a6bb8292e733810ba2d60b3521ec7c6a471fee0e5d5ae2c55bac3849754c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3823c9a48870bbe527ec61e77aa0cce736385ef480f16ba39c87a5611521d9ac`

```dockerfile
```

-	Layers:
	-	`sha256:8b1001c50474155b62c95f85437fb294965667469b18b7bbdd842661b8715201`  
		Last Modified: Mon, 09 Jun 2025 18:41:53 GMT  
		Size: 7.4 MB (7409281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5facc91781a4d2750f17b80d73b8e9861481cdd040000186b2cb6f45244596`  
		Last Modified: Mon, 09 Jun 2025 18:41:54 GMT  
		Size: 15.8 KB (15789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70a8ea6019ac4c0b8a65dc30ca6284892eb52cf210c1a85622565c5ceabd5bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227221551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9003b4d7921da7e1179ad079fb4c890dc8c1e6444d21a986dd7cb1bbc31e9365`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7537e79c58dbcab2941c040399879be549690329edde2c0c79c2f4b2c6e312`  
		Last Modified: Fri, 06 Jun 2025 12:15:10 GMT  
		Size: 89.1 MB (89091276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bba0313948318694bf2e813b0a4c677623c80a6a08f37ee813606b178bc6c3b`  
		Last Modified: Mon, 09 Jun 2025 19:18:31 GMT  
		Size: 88.5 MB (88510941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097a649b6fedd5ef5bd7c36fd07163d0cb683153293721a1b00b10d01b5b3cc`  
		Last Modified: Mon, 09 Jun 2025 18:02:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5124a732a3de50007a3cf1b7ed2005bcc153480b46930ded5ed06625c908bf`  
		Last Modified: Mon, 09 Jun 2025 18:02:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b287e421f6527cca22fcea0e3f27f57f38299cd530aec1c6ba53c8abe7fe6b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d4cba4901a6bf2344770f14526f82121270aaad990d53b30a149f079659b84`

```dockerfile
```

-	Layers:
	-	`sha256:23cb42bdc33fd8c6213f72b59c698f035f26a86b5e8d2947822c1b69763c4001`  
		Last Modified: Mon, 09 Jun 2025 18:42:00 GMT  
		Size: 7.4 MB (7416308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb7ef354673e9077b32cb6867db2068dbffb5b846975a3b443819e250ddbfef`  
		Last Modified: Mon, 09 Jun 2025 18:42:01 GMT  
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
		Last Modified: Wed, 04 Jun 2025 11:30:58 GMT  
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
