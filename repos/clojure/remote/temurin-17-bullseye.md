## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:e478c366e880a81a514663fbdf7911d8230dc6a3d24f64f6db464742ada7a2fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

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
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2abdb1f106b8c55232c616949e000c39831acc6b7cd6ea7bc9935580bc9ca`  
		Last Modified: Tue, 04 Feb 2025 05:21:14 GMT  
		Size: 144.6 MB (144566551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb689fcd61c815a91922541ea0bcb06cf68ff47c07e97b6def9094437b05b09`  
		Last Modified: Tue, 04 Feb 2025 05:21:13 GMT  
		Size: 69.2 MB (69190855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed634caab653d6743247a79b0d5fbeb780f585b5bea3fcac6c26855f970ae60`  
		Last Modified: Tue, 04 Feb 2025 05:21:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8691335afa41dffa05e197faeff6dac9be1a1517c338d86c2e1f8ea98a5ea4cd`  
		Last Modified: Tue, 04 Feb 2025 05:21:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

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

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bf55e279ee08aca8beead420ca4d1bcc0a488efcd2d02a87cd60eb057a01d0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265013387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07dda304ddad1cedba2f428a73dc08271a215a6f63dc8f0920301621c3bf7944`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e202a10626f68e896fc2fc05255f755ebb42f09c86c0284fd3b935e2bb7268ee`  
		Last Modified: Fri, 31 Jan 2025 05:12:04 GMT  
		Size: 143.5 MB (143454587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f5e70af75275501e2cce10769cce91c2afcfad65910c5deb9f1e1b7b802689`  
		Last Modified: Fri, 31 Jan 2025 05:16:44 GMT  
		Size: 69.3 MB (69311699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edde19f4ad21140fa353a4fc0a3328c6b4bcf71099e6d703afe20bd1cbd86ac`  
		Last Modified: Fri, 31 Jan 2025 05:16:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fd96dd05b891d0e5be10e11588c3e46c55bcbda41f53c370ae977a637958cf`  
		Last Modified: Fri, 31 Jan 2025 05:16:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7b7ff382e558726ed27e50d548473f327af0e570663082bd610b49ae184e4ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1c6cec938c9651a64bfe6bdb0e98a150bcf88fb080671a2398d282c796d76f`

```dockerfile
```

-	Layers:
	-	`sha256:2835112efca4c70f0865071e92a335c6f71785c54b323e04afbe9be7a70cda08`  
		Last Modified: Fri, 31 Jan 2025 05:16:43 GMT  
		Size: 7.2 MB (7209654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c194c6383045dd0172c6729998b72286534cff0e02e62adab75411c012514cd`  
		Last Modified: Fri, 31 Jan 2025 05:16:42 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
