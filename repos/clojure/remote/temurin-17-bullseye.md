## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:472d2a481d92e0dea515f1a185ba7109633a0d90067818ab26ec113ce0da5825
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a7f55c9c8faa957d952503b9127f1c483aaeddc65f7f1295686417bb3b37a352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269582716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea006e57e467ae8d18e1568d35ad679dc5f554d4c07012d2c7a60a89f97c55de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc73ed4c630fd3f3f5087ae9026ee4d41462b6683f884d9e4dfa53d99204d66c`  
		Last Modified: Sat, 12 Oct 2024 00:54:08 GMT  
		Size: 145.2 MB (145166553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2860472c0b87dd32872bc48e4a183e26fa982b54fea90d9df165b37d30fa7105`  
		Last Modified: Sat, 12 Oct 2024 00:54:07 GMT  
		Size: 69.3 MB (69333730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbe0306e54baf8a6ef9aaace7ab7bc8da2e37e8ab8e949b00006d132020472e`  
		Last Modified: Sat, 12 Oct 2024 00:54:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579afb1fdaf1e2718a93e8629a3a0b0a0a88e9d305483e1fc81443854416e889`  
		Last Modified: Sat, 12 Oct 2024 00:54:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e9cd2b439834ab6b39d7762bc8900e7ebb62239123173afde3bfbd8e0b264310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3fa0870bc508e7353dfd2ea19c2d51b75a6963531578a1ccaa19dc8093514c`

```dockerfile
```

-	Layers:
	-	`sha256:51bda0179b03c71111fbbf8fb474583870a473bc69070ed30e812b05e63fac0e`  
		Last Modified: Sat, 12 Oct 2024 00:54:06 GMT  
		Size: 7.2 MB (7189363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c71b9f89c1e46c90acfe36e8e0fc36c5f5ff78b7f7a26f8591be34f3047920`  
		Last Modified: Sat, 12 Oct 2024 00:54:06 GMT  
		Size: 15.5 KB (15478 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e985085aba60587d4ed284ce51a3b97c70108089415f3ec946227102dd9a7b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267161513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c730232091c406a056aab7da53e5a43bdfdefc217a914062d3bdc867b3039c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58a5da7081e969684b0f4da95120f470719256597a652148ed899f20250e61d`  
		Last Modified: Sat, 12 Oct 2024 01:15:39 GMT  
		Size: 144.0 MB (143959514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7758315b6392ed5e9a5086dc2b4cf32939abcbd16f9cc19be5c6f62b1712c4`  
		Last Modified: Sat, 12 Oct 2024 01:19:56 GMT  
		Size: 69.5 MB (69467092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf8ea82b0819800360337de4648c40a4e56706a5746d442f11dfbd1f0971d43`  
		Last Modified: Sat, 12 Oct 2024 01:19:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b75546bbfc5d924fbd7f5e7066f086f468c65a9552674d5cfa1d30f460d20d`  
		Last Modified: Sat, 12 Oct 2024 01:19:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c0a20286509f1895b41dbf5ae8ba8197c49d79d65f2f8d383fb25f0c3c17b663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9def24e05d88b1e40d2dba1537f6f4e8b8f55d84f8451d36ca75164bcedb6e`

```dockerfile
```

-	Layers:
	-	`sha256:929b820290c50c933ffcb48fd1fd7d04671860295421f4f48ea54cd7723b5b25`  
		Last Modified: Sat, 12 Oct 2024 01:19:55 GMT  
		Size: 7.2 MB (7194466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35ecfd1d9a758fb6e1f3fb5e91451ab7de4e08530b95ec4afe357326f649488a`  
		Last Modified: Sat, 12 Oct 2024 01:19:54 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json
