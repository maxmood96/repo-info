## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:14fdf583435ba30c6a41db43911670c70b826203544cd7971b042eb0f33e379d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d662635b960349360b73dc081ddf79eef25f4dbdcb5ef21e10be1243724cd5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273779192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f276d76a60ebf3c427b319318bd4b5b159e06f1e0254ab5c3d4a78237daac876`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05aaf630c4ced92c4d0f62cdcbee20563bf8665f5d4c5109c0665de94dc2b5d`  
		Last Modified: Tue, 24 Dec 2024 22:38:17 GMT  
		Size: 144.5 MB (144536708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0cd88d471f3301e4b23e457d41820589f85113bf3baeab6066ad00ee5041c9`  
		Last Modified: Tue, 24 Dec 2024 22:38:16 GMT  
		Size: 80.7 MB (80744376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5270bf8bb2d67a07f4d0c01469a7976e8b2b7a61b4bb240f83e0663ceb03802`  
		Last Modified: Tue, 24 Dec 2024 22:38:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531d487085302fbd21f6043916c9b20081b98c4eeecd1beda5e3db9d36e67705`  
		Last Modified: Tue, 24 Dec 2024 22:38:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cc6da30e0a3be1670ff6d13d94f3e44770ceae0281ba70888786462de9fcdd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4aeb7f0041e6457bc0248fff9f27343aa798ebbfa1cfec21bda41a76441bf8`

```dockerfile
```

-	Layers:
	-	`sha256:464fd0ffb6a81a1f5a1418ce62f9d1953680f7e4097b11629c03172e35bd954d`  
		Last Modified: Tue, 24 Dec 2024 22:38:15 GMT  
		Size: 7.2 MB (7171018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e94b07fcf79cf88f6222a25f24697d75dfede67795a47f29ce8d7bb987b6c3e`  
		Last Modified: Tue, 24 Dec 2024 22:38:15 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:102332af312ad6b1ec185f3d010d546d62487f0b2dd7bb24c3e331531ab925c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272293070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce688c0439f38879e4893d309bda1b6d4ca1429bab85216af7c57d126886060`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a64b07cf9d984ea02cce7f64d487e4828a776c450c76db8a089be6707a179c3`  
		Size: 143.4 MB (143361002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967d5a3b186352619fec45909998ab92704d663df04f20d6a0cc9d003fcf4d43`  
		Last Modified: Wed, 25 Dec 2024 07:27:58 GMT  
		Size: 80.6 MB (80605545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ba825b5a40b2c4bdb2432716e9f5969cd41ccbb6cfb142a65e66ea8436111e`  
		Last Modified: Wed, 25 Dec 2024 07:27:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9c54a4c25deaaff32f732463580090bde55d65069b65ad110f02ff9007bd14`  
		Last Modified: Wed, 25 Dec 2024 07:27:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fb35a11cab9ccc1cc589f2d21800a4a310558ac04df65af5cff63c0bfc3756c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ed6fefa6ffdb7060fc784b9c0a372a8e09677f539f1a563b72e0a504d8f175`

```dockerfile
```

-	Layers:
	-	`sha256:4b4160f8dad20bea4d10ba677f361c6d262e71974827cd69f37b9a555a59c604`  
		Last Modified: Wed, 25 Dec 2024 07:27:56 GMT  
		Size: 7.2 MB (7176781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eed0fb3ec1af7ed7d11939fbcdc9e395406e9eaafa6ba0e972c885c60cea845`  
		Last Modified: Wed, 25 Dec 2024 07:27:56 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
