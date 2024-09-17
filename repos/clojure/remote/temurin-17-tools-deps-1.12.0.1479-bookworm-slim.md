## `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:552ebd77be94f13a307126587acfebf6e7b898e5731faadabb35b389a5e18ec5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:43d9fabc2ec6892a8d8e65035912662ffc9172903f0e752b283952e848dc644b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243776781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74801bd922e5f3e3519522032847d89ba0556b157ba9a8e98598a7e0332956c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
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
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9f562e89b180edbc6be57a7435a8322e47b57c34fe3cf5cd7b46e2a80314c3`  
		Last Modified: Tue, 17 Sep 2024 01:56:57 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68614aac20695d9a2696aec05e96af93abb4e0080e18adaf3e2f4f9b7b4dd`  
		Last Modified: Tue, 17 Sep 2024 01:56:55 GMT  
		Size: 69.5 MB (69482696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2648fd336067f90039d8e23c52d78a2bc7a8c2192a62619b51d6f4dbcb1e91`  
		Last Modified: Tue, 17 Sep 2024 01:56:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b135299726185c9794818d4491b9bde6a9ceae8ce94ce623f88330e2ac0388`  
		Last Modified: Tue, 17 Sep 2024 01:56:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a6dc85000ba6ab62a226cd730e2c8113a431daad171f03723ba07561a8a998e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76391f81c86324a4c6c1e794287ced082074bf6c8c93e65084cf259cc3b390b`

```dockerfile
```

-	Layers:
	-	`sha256:f9207b5549d91439776a060f33738fd7f9c98b0fb3346217ca6fb0189a7b50bb`  
		Last Modified: Tue, 17 Sep 2024 01:56:53 GMT  
		Size: 4.7 MB (4745192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38920518cd7739d43734a58b7336f0401ec2cbf7c95c48cba3dfa9992dc30163`  
		Last Modified: Tue, 17 Sep 2024 01:56:52 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

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
