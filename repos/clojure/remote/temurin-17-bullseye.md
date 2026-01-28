## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:7490fc5fb5ddf453fac957553e8b051e9c4e3ab8f0124ef01016023a04dbde57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:65a1a9fc8810e262619a8c0349a74a5ebdbf65ffe8423c100734dbb0e5167cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268147311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6495426def31d146ee38ebe795a1c1c87387391fab3f3a8a0ec62bfecd9717e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:04:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:42 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:42 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:04:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:04:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4289994a77e828f49eb75ad121be08260b3fb931587461ff1ff32315abfd2b5c`  
		Last Modified: Wed, 28 Jan 2026 18:05:16 GMT  
		Size: 144.8 MB (144847973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2e09e0035142fcd74719c4e72669765dd0a41fd5efb366fb9cbd7b2ff19ac6`  
		Last Modified: Wed, 28 Jan 2026 18:05:19 GMT  
		Size: 69.5 MB (69541849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b27645dd7aef02285188e7d2ca526fbb8f1f31718f5298f6cf8ab9c79336b`  
		Last Modified: Wed, 28 Jan 2026 18:05:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031282587a5b9a2825e14fc6dcd454d729fcc3ba53e1412bdab2fde829db5e6b`  
		Last Modified: Wed, 28 Jan 2026 18:05:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d8e892ebff98326496ca8f70ad887c871530f1fc1c602dfa64b8ddcfe334c4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc05d56e76ed776e4474c76c753c2758fb8bcfc70a45ecd0dac1b9984ed6c84`

```dockerfile
```

-	Layers:
	-	`sha256:70979a680a1ac2c9db704c56753a9320252bf3b536ae7cf2832d8c14a7477b58`  
		Last Modified: Wed, 28 Jan 2026 18:05:16 GMT  
		Size: 7.4 MB (7396468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c2ca872592ce749ca89ace378c1538108007f0f4bdbffee8d2d4a79913c1884`  
		Last Modified: Wed, 28 Jan 2026 18:05:15 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f21b3fe56197ee881b5f9a5695828b54a85e3c5e7243d633d64a7a8588b12a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265632128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791a6215a1d0bed13550f6ea1cfe4184d357061a5d20d581fa7ab50083676bdb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:04:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:15 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:15 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:04:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:04:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bd383b92dc3a5ad6e303f259e027f5de3c5d2399df069006d0fc711d466a4f`  
		Last Modified: Wed, 28 Jan 2026 18:04:51 GMT  
		Size: 143.7 MB (143679942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1969d0faf9ccf66e6c273fd5b330ce643a31527c5379a3ae316d917f70c3a3b`  
		Last Modified: Wed, 28 Jan 2026 18:04:55 GMT  
		Size: 69.7 MB (69693377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaabd8676fa1a28d095b7e0c6891aaf0bea72c31174276aeb3a7ed27c2b4804e`  
		Last Modified: Wed, 28 Jan 2026 18:04:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3168a7c4cda350cb421c96dda39e4c3d256eefb975c03c0c79850a7de75efec`  
		Last Modified: Wed, 28 Jan 2026 18:04:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:46c9a15f5d13745ec73149011cdd4977a45c52b7946082714034b37035148ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f88c29576e3b464087997522705d41439174a76396cef2e6e0326dfb206afc0`

```dockerfile
```

-	Layers:
	-	`sha256:17d121c2c2014a34e1806b53178edfd379b699fdf55aa14220e4c489d58f74bc`  
		Last Modified: Wed, 28 Jan 2026 18:04:49 GMT  
		Size: 7.4 MB (7401567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51613a9850a8370faeb4d600223ed0b66ce3b909d6b23d444205f4fe562a03bf`  
		Last Modified: Wed, 28 Jan 2026 18:04:48 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json
