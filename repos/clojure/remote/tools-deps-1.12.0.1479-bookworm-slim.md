## `clojure:tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:9c73f28880faab7560b1d94ce053f132090e7b56158e2c2e8fb493778b5ba0ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e3399ca9e9db5f984e5db4d21bfec39e337da82d3ec6232630ab4186ee9242c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257189592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4b82fa28fbe3d2cbec1f57153e984e0b70273a6f725eeabbe942cc86f7e899`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d239d93d81e78fcf7292d1df50807930fd680355fef94ffef3c2c6c2242b17`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 158.6 MB (158579307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f619b0bf094588bf8812d45503982060ab16ec41cf7b4f6a80ba7b01d114aa96`  
		Last Modified: Fri, 27 Sep 2024 06:01:22 GMT  
		Size: 69.5 MB (69482972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5649c458d2d4377b85c28a9ddbeceaed20cecb1dcff13fa0fb9c616e2b455811`  
		Last Modified: Fri, 27 Sep 2024 06:01:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd97c9b74394a210843772cef8f61e1745430869b3dfe27145495c0bf20c185`  
		Last Modified: Fri, 27 Sep 2024 06:01:20 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1cafbb524e27bbc171f208b291b1b19dcd457ab7ef2a988317b65c2c033fe363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4914857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bb59b6b1b9d0099c164097a8cdb06726e65d841d0bf2d5b5b92af4fac64453`

```dockerfile
```

-	Layers:
	-	`sha256:72d0a60694354bb387816822cdf83a5adb2d1fef9858e523b82f34f7569f2e1a`  
		Last Modified: Fri, 27 Sep 2024 06:01:20 GMT  
		Size: 4.9 MB (4898648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b87de6336d21b141171518b810054c1ffe2f48fdafe6bdc69ad11305cd67d24`  
		Last Modified: Fri, 27 Sep 2024 06:01:20 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cfb0a5563c98592b67e56ae98d3dada4663587ed37b4049d95a4fe642d082f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255248395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674650ac692c131236e80be2b8016bf1c3b73cc3b51e64f2c12f3328f9763014`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852185c1f9892de54ba89016ebfc06a6aefd5aa5906fbac5eb84e6d025cf0c9`  
		Last Modified: Tue, 17 Sep 2024 04:42:09 GMT  
		Size: 156.7 MB (156746196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ef52e8ceee47906689e9a4389c6e552a9095f14b8263bdbc5fd191b23405e6`  
		Last Modified: Tue, 17 Sep 2024 04:47:47 GMT  
		Size: 69.3 MB (69344609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33518a6047e02f05fad0206db6b9fed1b301bcfc7e5959b32ac3008284b3c186`  
		Last Modified: Tue, 17 Sep 2024 04:47:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13785fd7cf1263f89e07e331338aaec1f5b2989431d78ddf40806cdf2e15eb0`  
		Last Modified: Tue, 17 Sep 2024 04:47:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:48f1c01737bdc327807b27dbf4a762b0e22f3661cb28e272054f0291a5d9eb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4769081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e4c100a799daeaee10186486e5c61a888118ccaf3d99f979150af14ff05d71`

```dockerfile
```

-	Layers:
	-	`sha256:55386e9abc3d0fcd44d3d3e2aa8708894c1dd92c397118f902c5031338c7aae1`  
		Last Modified: Tue, 17 Sep 2024 04:47:46 GMT  
		Size: 4.8 MB (4752307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6126ccd363695f5d69facdc7d50aae232d31e227ea3cc025d6a2b014772d662e`  
		Last Modified: Tue, 17 Sep 2024 04:47:45 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
