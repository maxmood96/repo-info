## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:dc70d7c78335af4093ba07a478845caa2d14847735f50121de0bfa7f09c0d818
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:13725a52de5290f74a4f9d08f5dc452e9ef71415c79df42fa2e820fdb93d7ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177651720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c34055da09d9f6922fe4069e304f1e1ce2143c7993f24dc4ea55f056c4fdb3`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0615cdb1f0e4320384c5d4d6eb2f0e5111f1a0165c6d6ca0995a53d282adee5`  
		Last Modified: Tue, 04 Feb 2025 05:28:00 GMT  
		Size: 54.7 MB (54721284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa58f07f115cbe7da3e858822166ce193a82c53a69f55dbe1df45a2bbc997f41`  
		Last Modified: Tue, 04 Feb 2025 05:28:01 GMT  
		Size: 69.2 MB (69190918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fe94bda56b0ae7ec709c064ff1fea76cd92f46acc3ad790789acc5f5982327`  
		Last Modified: Tue, 04 Feb 2025 05:27:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:96c5be131c10013126a91babc01a85211391ef8281bb4b23d44eab377cd07c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88e0c1f8b748f58bdcfd1e22ef5d5174bead954242e4904d6e5eb078f6e6918`

```dockerfile
```

-	Layers:
	-	`sha256:3bc5d1402cfbfd79ce665bf302984cb7521cb644649743cec06de1bbfb1bf0cf`  
		Last Modified: Tue, 04 Feb 2025 05:27:59 GMT  
		Size: 7.3 MB (7326165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a62659ca740a009d551edf193a3044c160dc8a5b69a0553f6a66a9955b72c167`  
		Last Modified: Tue, 04 Feb 2025 05:27:58 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a7ea02a9be24f8d5aa5b6f44b3047fa6a35c0b3b1071594b2e8234345bf41598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175381080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1b6ce0184663f58e9c9b02d1cd6ca0489b7c7dc6e13bf21b98564cc161c5fa`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4479f04fa46a0a97de41bf437ee5aa33b614660ac4d56b2619544364c89cfce3`  
		Last Modified: Fri, 31 Jan 2025 04:53:18 GMT  
		Size: 53.8 MB (53822735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8161e3bb25466cf6982eb49432fb9bc7c9a0f68c0cdff877a3e36df02b83663e`  
		Last Modified: Fri, 31 Jan 2025 04:58:09 GMT  
		Size: 69.3 MB (69311640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41b9cd63c0423ab81669808e64854018c3d8c5dc11e2bf2c47d7ba02fab7f45`  
		Last Modified: Fri, 31 Jan 2025 04:58:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3ae6835921b90e97acf80d42c5f44d236ce7c2b8ed652a1a37103cbcc5ab2fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fe7350279f85e7f287d4010258c083360df732d0dc6c674ccdb1651decb91b`

```dockerfile
```

-	Layers:
	-	`sha256:fe9accf4d6804dcc08df28e53d77783ff8e3495507f4f6c94a5bcb6249d85fdf`  
		Last Modified: Fri, 31 Jan 2025 04:58:05 GMT  
		Size: 7.3 MB (7331962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:613ad249395b195b51270f7a450c166e6ff2fb316c42398662b38b7186683d6f`  
		Last Modified: Fri, 31 Jan 2025 04:58:04 GMT  
		Size: 14.4 KB (14354 bytes)  
		MIME: application/vnd.in-toto+json
