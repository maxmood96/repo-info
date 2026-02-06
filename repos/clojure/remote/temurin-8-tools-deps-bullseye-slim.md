## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:9d5e480fd9b999c98ebc55f774a3b50e4af8b6d161166b132264695726607b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:14ad2f2b3694616bab1182f667d1cd2ba3805486f2dd21c10c8b507a13fe0474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144565528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d3de4c5e4ebcf6cd4bedb87a1f294b35bb42aae19fc8a2acd9f0e51a5dfa1b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:00:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:00:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:00:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:00:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:00:27 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:01:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:01:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:01:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6758e1631d321df91953fb2b92a7e3520264668758f98ed2a0296e5d633bb9`  
		Last Modified: Thu, 05 Feb 2026 23:01:03 GMT  
		Size: 55.2 MB (55170117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fb9b7bb91c728689ec33acdbd9c0425592820254b226e3b45374d5f73b1138`  
		Last Modified: Thu, 05 Feb 2026 23:01:40 GMT  
		Size: 59.1 MB (59136481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2637d246cd966fc1afbc9a2a06824affb244f343916faa63a96d687a5d77278`  
		Last Modified: Thu, 05 Feb 2026 23:01:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a195755904e47e06aaea28adbd2baeef7482c7c10e391bffab3bf6e9d889fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96c52b1269c90c11957b6a94a1458222225bc63f73a115ddcb3841fcd375c6d`

```dockerfile
```

-	Layers:
	-	`sha256:2413ece58ab868a3369e65284852e75b4d2a7325b2406d1dabf613b59b730b87`  
		Last Modified: Thu, 05 Feb 2026 23:01:39 GMT  
		Size: 5.4 MB (5431107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1975b7a32e886c21b621900ef303d92786ef99b862d40e403fa65f1bbd7855f2`  
		Last Modified: Thu, 05 Feb 2026 23:01:38 GMT  
		Size: 14.2 KB (14246 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46241e219c5f02f6764452cf74e4e1e524a278b0fa9375be204b754170c1f31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142284761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e794708655799c4966e12dbec5f9fd991af086ceb876e05e4c52b1db581bc0e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:02:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:28 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:02:28 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:02:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:02:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:02:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41bc612a886e9298291289cb8a0273a1b5435f561a60ad14c2dfca06eab22dd`  
		Last Modified: Thu, 05 Feb 2026 23:02:59 GMT  
		Size: 54.3 MB (54251630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb020444a0c7b9a2e684f6ae7c0edc0ce6feafd225b908f3de8d05f8e37a2b96`  
		Last Modified: Thu, 05 Feb 2026 23:02:59 GMT  
		Size: 59.3 MB (59288047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d8876abae956e319a695cff758993bb352a917bbfd99550ff3221540e3068`  
		Last Modified: Thu, 05 Feb 2026 23:02:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c2d58a0cdd80e854e32167f92f10cca29f1f8f640d820aba7a52155f0e9bba39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13dd7f3e41db8d26adee4f77e73298e15b1dc7c099ca332035f77d9fe484213`

```dockerfile
```

-	Layers:
	-	`sha256:02ec26d754dce700cc66f51e283d6c86a5f1156245349572170d817e73cfe6d9`  
		Last Modified: Thu, 05 Feb 2026 23:02:57 GMT  
		Size: 5.4 MB (5437539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1482cc6deabba316668a1ed2387adc4d4566f22389e680bc4c3b8847963190e`  
		Last Modified: Thu, 05 Feb 2026 23:02:56 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
