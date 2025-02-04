## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:6ac8053c92546cb51dc97d29729cb5e68aa8fc7993a21d065bda0ef7ae777a21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:199178b3e01aa58e9e356131ad36cebc08a7df9a08e0d1c7e4223d0b9d87e4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287060360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422959321589b2b88c5b8fc4b99af40596c6bd2e3427149c34c2a8e99cac0cd0`
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
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debc1dc56cde66ff720e4dea91acb24e97887ea4d7beccc0bced0a4c60a0bc4b`  
		Last Modified: Tue, 04 Feb 2025 05:21:37 GMT  
		Size: 157.6 MB (157585929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a401d16fa58598a0c0a9a5e949e084d4ca809ca685a611c2d122e1c578b97c02`  
		Last Modified: Tue, 04 Feb 2025 05:21:35 GMT  
		Size: 81.0 MB (80993703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2f1e55064adbdacc8acd7af4d4fcf6713f910cd91697efbe3a1b7d7a80ea3d`  
		Last Modified: Tue, 04 Feb 2025 05:21:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b5bb6b64ee0070a9e04b511f2ab3fbdf853158b716c106b52c03c9c8e0215e`  
		Last Modified: Tue, 04 Feb 2025 05:21:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:79d0b6904bc0dcf860c7736e0df870d902036937efae2e16c783b6037a631624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22a29f0e65054674bae787cca659d68efa4b6f79315a33b975dff5f0b1e07a2`

```dockerfile
```

-	Layers:
	-	`sha256:172232bdd6e321542ebf5763ca2aa1ce66cfeaa2c3bc6d3582bbda651c95270c`  
		Last Modified: Tue, 04 Feb 2025 05:21:33 GMT  
		Size: 7.2 MB (7176180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d5e43df7e3f8d126ef2b6722d519a1b60a3672c21668474f7141207ad1b85a`  
		Last Modified: Tue, 04 Feb 2025 05:21:32 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:07ab6b8ab8f06456f42b12d985340ceaa700ee6c508d38755f7e1a10b7621426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285012966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28108f332fdc30b7e4f9e3223c9374076d07fdb61304ede2cfde58f548baaab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c34e075e37e524b436802c62baf0679e4472bcdb458b6ac93c635e1e1afa9b9`  
		Last Modified: Fri, 31 Jan 2025 04:51:37 GMT  
		Size: 155.9 MB (155859318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b1364cbe24c3f518b6585c597b31c577d224da4b51225cac01a4d39e88f5a8`  
		Last Modified: Fri, 31 Jan 2025 05:24:15 GMT  
		Size: 80.8 MB (80845714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed19fe02177bfcdf4e3c1d87f4785530a429e8a9620ab0babeebf12f593a3d3f`  
		Last Modified: Fri, 31 Jan 2025 05:24:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543c98abed75c063284479c557354f45f19e4c789be146eb7ee6b87d40c4d5cb`  
		Last Modified: Fri, 31 Jan 2025 05:24:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:589bbeee94be98884ab039c178f16201db19a3f0d25173be067261b00f2d020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8025a0ef1a0f160b5ad36e8a0f8956269826cc8e42d5ef886c9f7ffe018fa130`

```dockerfile
```

-	Layers:
	-	`sha256:0269aa65877db5c5aeb48cd10b646b482c887c7cab7c92afa2bdf877a896a425`  
		Last Modified: Fri, 31 Jan 2025 05:24:13 GMT  
		Size: 7.2 MB (7182015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14891f96fea4cbb1d4c0afa70334aa1f4bbcdaa0155bc48884107c65ef2a6190`  
		Last Modified: Fri, 31 Jan 2025 05:24:12 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
