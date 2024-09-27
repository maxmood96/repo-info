## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:8e125cbcbcd42d66ba327fb28d38e5cdafd135790765375a3875cd0748698048
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b13df6c0981f755b070f0049076a4fc989361537f6447a453c8f061001089022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243776647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d65ccdf066763fdd5dd571965f94550d634f1f241feca2cbe42bc80b857936`
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
	-	`sha256:0095f8a545bef697e105e67c2d9706822fdc397383573ca660b3e95fbce34385`  
		Last Modified: Fri, 27 Sep 2024 06:01:16 GMT  
		Size: 145.2 MB (145166557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2768cb41e5c36ff84d6fb38fdacadbe4299ad290a2e971894d4acb812aeeddb7`  
		Last Modified: Fri, 27 Sep 2024 06:01:15 GMT  
		Size: 69.5 MB (69482776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11083af72f66c456896372c48766224a6dfc23ac76353d80359ba87e5d22c1cc`  
		Last Modified: Fri, 27 Sep 2024 06:01:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6464cbdad27bdc4bd3e7efe093254de8d76f1c23b095f2ffd0117d4698436c24`  
		Last Modified: Fri, 27 Sep 2024 06:01:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8cc810d8d8adc367459db7dacde5212316061eeed06a6b95a47f29e9eb44773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4909723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa39146dbf3d60db71e014a0a9e86f332be65e8c648185852dca79b762953c2f`

```dockerfile
```

-	Layers:
	-	`sha256:801b751a6a12c9172b17b2e59d50b34c8214e28795de1f3fe1d3b89c5288235c`  
		Last Modified: Fri, 27 Sep 2024 06:01:14 GMT  
		Size: 4.9 MB (4894211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175b1d2d93a455b7932f9e4d4a0fd939107247e7e90117bfe946ffe2c723e280`  
		Last Modified: Fri, 27 Sep 2024 06:01:14 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:866618d36a223e4bbebd990b65386f14be95d86cd4adca415476b416bcf03cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242461679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b69e63a21cc5a5c28ed2e1ec5f6e0ae3a211d2fba28d4b9dfef552a2df6a55`
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
	-	`sha256:03eefa106121aeb9814b7bfa0739b5c8f73502aed3ddc6b655d7f993b668b368`  
		Last Modified: Tue, 17 Sep 2024 04:31:16 GMT  
		Size: 144.0 MB (143959492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219029e69fbb3b8b715e3e32e175c26d4c5e7e215a906dc4ed309988a4d9d64f`  
		Last Modified: Tue, 17 Sep 2024 04:37:29 GMT  
		Size: 69.3 MB (69344596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a18d32e2f5cdf5b449511e904cbdca4898f89795a850e78c2c6f4bf19ea9b17`  
		Last Modified: Tue, 17 Sep 2024 04:37:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c6af4a0e0b046257484f6e031b4ba7592daa4b6d9f1202dea63bfb37ab7db9`  
		Last Modified: Tue, 17 Sep 2024 04:37:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:347b6dfe86de6fcb9bb06a88692fc5bbf1a81572a2c0fec9d7f44666e5b508dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3ff1c6079b0cf9ed1c6380dd64a4889ecba923cd113504275eb9173f2c3260`

```dockerfile
```

-	Layers:
	-	`sha256:63bcb2b1ff7850d6be83bac725fff23a47558e5078bfda766a40f2059a60285e`  
		Last Modified: Tue, 17 Sep 2024 04:37:27 GMT  
		Size: 4.8 MB (4751577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f1e4ccb056d6de7d634963cf09ddbe143ebea712dab0cf73aff8e6e19161d18`  
		Last Modified: Tue, 17 Sep 2024 04:37:27 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
