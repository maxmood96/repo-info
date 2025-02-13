## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f0d4ffa82fca40952d5fa0bf49e4a0d942b63c667036f65641c2ab5d4de861ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:767d0ebbba32b372b382f5876713b77600164d4846186f7d69a2ae2c9d14d688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267497319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13540882dbb43b3208774124feea6bda443c796d4bda82415b1a5e18da78a104`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 04:23:03 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2abdb1f106b8c55232c616949e000c39831acc6b7cd6ea7bc9935580bc9ca`  
		Last Modified: Wed, 05 Feb 2025 18:09:53 GMT  
		Size: 144.6 MB (144566551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb689fcd61c815a91922541ea0bcb06cf68ff47c07e97b6def9094437b05b09`  
		Last Modified: Tue, 04 Feb 2025 21:51:46 GMT  
		Size: 69.2 MB (69190855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed634caab653d6743247a79b0d5fbeb780f585b5bea3fcac6c26855f970ae60`  
		Last Modified: Tue, 04 Feb 2025 21:37:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691335afa41dffa05e197faeff6dac9be1a1517c338d86c2e1f8ea98a5ea4cd`  
		Last Modified: Fri, 07 Feb 2025 08:50:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c925b51a84c6793a00a77d73a986ec932957271ba01e65b82e9dbdedfcc913fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7d3dbf1fc808a6fa75eb9005046022692dfc52d249758ac228ac5d48278d3b`

```dockerfile
```

-	Layers:
	-	`sha256:74bf2d15a676113e07a22e10fdc51e088d2334f60fc9ff48be6fe218d9fdbdbd`  
		Last Modified: Tue, 04 Feb 2025 05:21:12 GMT  
		Size: 7.2 MB (7204555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76689b9974e66591d79005e23957efb2978049ced02db096f77d127714778ebf`  
		Last Modified: Tue, 04 Feb 2025 05:21:12 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:86196c7700e10523502eec6b6d2549d7482e7e68d568dc078f5d4f8a215cb61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265012897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1c8094d873a9e861e5d26c1c1448719463c23c8e1ebe4ca0fb5de394ee2b60`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 04:34:59 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1708d5129285b28e8d76370a0f7735985e646f6353ff58995c4404eb7c7ac`  
		Last Modified: Wed, 05 Feb 2025 21:46:56 GMT  
		Size: 143.5 MB (143454660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39560fb74b574751e873c26d9c156c196fafe6e9999e6359e77cabdbfbeddb74`  
		Last Modified: Wed, 05 Feb 2025 21:46:55 GMT  
		Size: 69.3 MB (69311506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbc58b13c5b375f0ebfa8875bf0639867bd26463c955f67bf0ad5f2aad9e6b`  
		Last Modified: Wed, 05 Feb 2025 21:46:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5af8eaaa3ada1c09a2299c4e0a33570ecd11e3f8c72371bbc4caac17b91a6d`  
		Last Modified: Wed, 05 Feb 2025 21:46:39 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2468ae13b80fb59436c4fe9b30cf19dc00ae5571bd513088f0402983ac03000a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bf5f61c8e092dd29a2b3889c9cff863236bcfacd743eb18137f7ade63dd6ab`

```dockerfile
```

-	Layers:
	-	`sha256:e62a7bec363da7296c155c54a329248ddb63cb4aadbfb3e056363a7d96f10631`  
		Last Modified: Tue, 04 Feb 2025 23:48:50 GMT  
		Size: 7.2 MB (7209654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06717245562fc8a7184ab41f049666fc74338f00932072371266eaf99ade340e`  
		Last Modified: Tue, 04 Feb 2025 23:48:49 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
