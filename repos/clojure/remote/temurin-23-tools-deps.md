## `clojure:temurin-23-tools-deps`

```console
$ docker pull clojure@sha256:4bba485811634066168acf98ea88761edf3960b28f300c4e0e75482ace406186
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:6c89d6f4d135b1093a58e33eb92f280cf55cad597cf00d66f7e90b6b861cd990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294790807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cbee3d4f026388edc0e3f5f0b223ba8af691f4095c6527e6251cdcd98bf4ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5677422e15f022261e12225e1b7497c6f0c894f6a02923084d2b10421534842`  
		Last Modified: Tue, 04 Feb 2025 08:27:37 GMT  
		Size: 165.3 MB (165316181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b67f43b231dfead60ac1d7cfe8a4b483f3ae767447e97c1fe8047b9a93324c`  
		Last Modified: Fri, 07 Feb 2025 07:02:13 GMT  
		Size: 81.0 MB (80993899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d417198751c159f59371031d98c01fd82088982a21dbdaaa528ab3d2fe64c35`  
		Last Modified: Fri, 07 Feb 2025 06:56:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d36bcb7435921d7a0f49bc6862bf092722a664e61eeaa87566438012109f72`  
		Last Modified: Wed, 05 Feb 2025 17:56:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:5ea9d4fbcecd5b55ba13c8aff639a4f02a8051c354efb4474910a59cd3dcd751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6838fe5fed4405de83bffa944eaa4bf9f08c916231f5f7eda9bdd1fbc3ad9aa8`

```dockerfile
```

-	Layers:
	-	`sha256:1a1315dea731b4c3a7632575f7849ac26a9909e15c8c3e57b8a62605c87fd907`  
		Last Modified: Tue, 04 Feb 2025 05:21:40 GMT  
		Size: 7.2 MB (7176767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad50c398349e79fb01b44dc2d42dc142c7635599ff65573e09efe84f0394ce9`  
		Last Modified: Tue, 04 Feb 2025 05:21:39 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6a3ac244b921d006d94ca28523824efe5c49ba5429ddf4ea5000b219b14cc94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292494810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f3f252dfcec47de7aa273a101e951cd3e3a08c172a7627e83111dfbdf475f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca50648c20ef7fd0a5ed1545a1006f88f616c5a3affb90331185a9a998f1dce`  
		Last Modified: Fri, 07 Feb 2025 07:02:43 GMT  
		Size: 163.3 MB (163341440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb2215b9c5ec4a19e6467805faf3d8129a96bae12431703b9d5de6b32c9f021`  
		Last Modified: Fri, 07 Feb 2025 06:57:30 GMT  
		Size: 80.8 MB (80845777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a4e842c6845ef092a9575c363d5d3cda2466e7581afae53b631dd230f9ed31`  
		Last Modified: Fri, 07 Feb 2025 06:57:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eea2a1529507dc4e9922b1b646b373198338d635a19fbe63a953b134a91de27`  
		Last Modified: Fri, 07 Feb 2025 07:03:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:b53cc2e449433f1c45ef0c18ead2cf46f90aec51d0b783b18e0bf7adc0d6e703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de7336269e25cdc65afcbd3204abba71d18cb990a804a5e4e0524633c46f42`

```dockerfile
```

-	Layers:
	-	`sha256:d9b18afaf442d5342b22399c783635f5b11d3356ae10338c066169db29ea5f7a`  
		Last Modified: Wed, 05 Feb 2025 00:04:32 GMT  
		Size: 7.2 MB (7181933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c825c818790db22c8dab1b76160051bdf0aae79d4461e9861ec9ffbf7a0c3130`  
		Last Modified: Wed, 05 Feb 2025 00:04:32 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
