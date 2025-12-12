## `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim`

```console
$ docker pull clojure@sha256:8dc5c0a1e3a3ca9ec19b8ae04cd599ac4a9ee694715a1d6a2a25153e23a90237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3915e605d36618347e95f6c1f0d50b3c7a7c4b8847c8571e625f4b6268897121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156502588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dacc975b6f8a2188113f8d859981d7bdff4de04ab256f53bc17302b94306de5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:38:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:27 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf03c19343dc5b1806715cc88d969dd89d062515c50207dd615690f9ea8b7d0`  
		Last Modified: Thu, 11 Dec 2025 22:39:21 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571db6d1daa89334da51f92ea8f7541fd4d56988d81218a566be5335cf436784`  
		Last Modified: Thu, 11 Dec 2025 22:39:20 GMT  
		Size: 72.0 MB (71992075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7092e5131a4ae087c5b69964b4adf84dd7e94bde9a17a65f2e00914487a2d11d`  
		Last Modified: Thu, 11 Dec 2025 22:39:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b710bb5ba13fc2741dfe7217aaad2c30a65209c5e2eb30827611bfd1da322b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06191cff6f64ad74a486334edf21d6cd81ffac63e5de51fd82382088189710ce`

```dockerfile
```

-	Layers:
	-	`sha256:968127c19bd4a2cbebfd1f33a918f320be6d82a9a926e7bedba709ead134ac61`  
		Last Modified: Fri, 12 Dec 2025 01:47:51 GMT  
		Size: 5.4 MB (5377807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e61f0a69af0b5990c2e13e279be980302b912c522d8df006749856ba3a4cf25`  
		Last Modified: Fri, 12 Dec 2025 01:47:52 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a78499440f02e20645683a6960f2bea7ce4cd9de5477b8a0f8b9898f046067df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155760996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5280665c54faf35464d38e40457937565386dcd43c8593eb07cec6c661e9ce`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:38:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:15 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:15 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675e12200e24e300b3f728bf337367ccef1883a1a87e0f28d0066da330972c50`  
		Last Modified: Thu, 11 Dec 2025 22:39:03 GMT  
		Size: 53.8 MB (53814993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5675ff90d87614bf17532b7dccafe8bd9f1bdc80fcc2cbb0e0b1e24a70df3c07`  
		Last Modified: Thu, 11 Dec 2025 22:39:03 GMT  
		Size: 71.8 MB (71806730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ff5a39108c263e86aaa19dd3f9135ad842f3f10ac8160d202b15e8c21d1f03`  
		Last Modified: Thu, 11 Dec 2025 22:38:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b92cc03483fc0bdf4be6b46d2683ae3aca98bb485c42a3152c8bf8ac70d1d34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3186009c6fd967d2ae69e2b8c2a6ae17388a571c0f3c5700db161fd61c423b6`

```dockerfile
```

-	Layers:
	-	`sha256:99a7d7fe31bfc23d3ee1a8ba1a677c8bb933d23807d8dcaee58ee3e490a5ace5`  
		Last Modified: Fri, 12 Dec 2025 01:47:57 GMT  
		Size: 5.4 MB (5384274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de2c2007a8abd444393a3e98f19b276febb52aa5591d9bea3e14647cbfd1844`  
		Last Modified: Fri, 12 Dec 2025 01:47:58 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:18f3646a012146e14ca55b07f990077ee1a55c0b92f50f8c2f74fef5dec27221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163159739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d47a8b560cae156a0a03741b158b0166daf7f4c9d2a9ef7c7d8dd2ece73704e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:46:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:46:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:46:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:46:38 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 03:46:39 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:48:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:48:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:48:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9ec5d91b1da27248b6474c55829b4ad5637900f96134ea7cb65096baa6ecbc`  
		Last Modified: Tue, 09 Dec 2025 03:48:24 GMT  
		Size: 52.2 MB (52175138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784452e94d901c952e8cb438b870fb05e7dbd5e497eaeec9ccca57349da1dc31`  
		Last Modified: Thu, 11 Dec 2025 22:49:16 GMT  
		Size: 77.4 MB (77387064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90d9667f29fe0a0243c185bfff2c1e163ea445967e2a9068dc0848539640d3f`  
		Last Modified: Thu, 11 Dec 2025 22:49:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1fe3faf8e2068e088afd10ecb26c30afcb79ba413a30002e79503fc7a9d21733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d949e577decd53cad4847e028c7954eaba8de1911afcee85d6936fefb2df4109`

```dockerfile
```

-	Layers:
	-	`sha256:2ed3adaef2d19bd3eed2e371c16cded07fe0f976d2dd4f76c81c43b186910e25`  
		Last Modified: Fri, 12 Dec 2025 01:48:03 GMT  
		Size: 5.4 MB (5382771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200dc0d21cbdd721d6f331a98a97c7170454a1979a5b4bc7aa7e7fa79f709e1b`  
		Last Modified: Fri, 12 Dec 2025 01:48:04 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
