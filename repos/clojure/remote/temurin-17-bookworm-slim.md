## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:ab14523fe19433e93d7deafce684b7f291e8f12568a1b4f464cade8cb82abbed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c3bf3e20e25bf9121ac21615c0217876c0bb985246af91828f74f5b71e71e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242061985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250870ec9c03c5332520e2c00d0b0628fb670992d8cbf0c86087a3983c00ad55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c493070157550d28ab55aa355583ee57bcda99e6eeb4c0347be50863926de88`  
		Last Modified: Tue, 03 Dec 2024 03:19:56 GMT  
		Size: 144.5 MB (144536645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf37d405c146679c918e479fcadc4bd3f440b51ff0535c76f09d2dde4e0428a`  
		Last Modified: Tue, 03 Dec 2024 03:19:55 GMT  
		Size: 69.3 MB (69292721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57e231f12ec9cd6abdbcd7b722cee064f16d6cb6e8d1c6f9678e83f0088d77c`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f598324f1b4673c57e87e035ec4d87fc6c28d3d537eeab80163cd8d1ed91b5f2`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d70d41eff01ae39d939b253362c66cbfbcb8f4afd97c298a45fc746ef2cf865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07642b763f1a90e40f997ddd760962b767278c83be53ceedf87b96a152c2afb`

```dockerfile
```

-	Layers:
	-	`sha256:ca992ef7be3871db9b9ed8d9f0148afba060130eef5bd1a2d66d75bc17583565`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 4.9 MB (4919380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c13de99c1233897f569dc05bbe4124ceb388a149814ef94e35a652cd572998`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c1cef7b8e220cdec4c88bc2d3af38939365c7eed1e3d8505c7d54c0989c9de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240561553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af81a3b9d7bc4f4c31faf412839b3da9533ee5ecfcc6ef7b5ce0c8858c476fc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db3ce0e9523a9eb5dc5d8c6b79f65c5c8ba65627853d1041da5183adb9a9e5b`  
		Last Modified: Tue, 03 Dec 2024 15:17:35 GMT  
		Size: 143.4 MB (143360979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cc1cf0a15f2e4f272cc6680feaa571ec8ae03c944ff724c3f6e1aac43ef49a`  
		Last Modified: Tue, 03 Dec 2024 15:21:43 GMT  
		Size: 69.1 MB (69140727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd1b7eff43d0f2e5a3552886ee7296c9ab61cd40772e9400dd4526b3500044a`  
		Last Modified: Tue, 03 Dec 2024 15:21:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9917055c57d5a95cc6baba828b190ea0d038251f6b98fac91d8df47172205c`  
		Last Modified: Tue, 03 Dec 2024 15:21:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b7c21959016ed07209d59f625e30b41c91aac759f6ea1c6c349fb01d296549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a9cb3e1471245ff762f18d89418862d8ff199f7d61ed97e8bde775a16b1b2`

```dockerfile
```

-	Layers:
	-	`sha256:3bf9141f8f34707c23f21c0f1881c5364e83d0e4cd27c7030e21126e5922c920`  
		Last Modified: Tue, 03 Dec 2024 15:21:41 GMT  
		Size: 4.9 MB (4925146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7dcb20920ae5b03d8a6faf1167e871d2d5a8f5e589de87afe54f5afc7431ec3`  
		Last Modified: Tue, 03 Dec 2024 15:21:41 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
