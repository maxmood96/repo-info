## `clojure:temurin-22-bookworm`

```console
$ docker pull clojure@sha256:2f58a7f2e5c68938642b9c6b51196022097027309385cc484fd1a5da75961a71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:827f08bdbbf463856b7e9c918a392962554c62da9fd57dcfe9da1bfc0dab844e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286490715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c3870042fadea12595878f8a3ba89cb8650853e1e5d2a7423ff9d7ec107279`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94dfeb6aeb6328b53d1a09965324882d4abe67001c86b538631ab10d536da56`  
		Last Modified: Sat, 17 Aug 2024 02:04:29 GMT  
		Size: 156.5 MB (156481638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce47683cb96d7ecf647a7bfeaa072d7a1ff03eaaca08ecb35bdc64a81c360f1`  
		Last Modified: Sat, 17 Aug 2024 02:04:31 GMT  
		Size: 80.5 MB (80453955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caeb0333a6b4405000ac007666254dcc8c87a5f3ed3221e1d6f50e0f5d88f5bc`  
		Last Modified: Sat, 17 Aug 2024 02:04:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fe0fc547d47a318f41b24678ae2cfa98269cf93512f177684de8b75a272172`  
		Last Modified: Sat, 17 Aug 2024 02:04:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0fa0272945ebb99930608b045813bc594dcebe08bb466e8e62397e12cbef4bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f2611cc907b6e372ea106942e75586f4f0c0f39d1c0ceab76c5ff5b4149018`

```dockerfile
```

-	Layers:
	-	`sha256:9343570597bd9e3d002587b12484ff2d119ad5a9a92af33e9f12b556a1472cbe`  
		Last Modified: Sat, 17 Aug 2024 02:04:30 GMT  
		Size: 7.0 MB (7000764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855beaedec236e050d6ec56ea7fc69ae88cc11e47d76ec7e3577cb9dc45ff13c`  
		Last Modified: Sat, 17 Aug 2024 02:04:30 GMT  
		Size: 16.1 KB (16124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:994959c45f27bb4824338bdbc43e812a9047d1939391f25f59f0e68163bc8331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284291771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f211537bdbd3cb41a325d11d07357a9361f96014c35dc9ea4d8d47e612bceca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648268b85fd4c094d06e828855a5f546b3a97f5c94583775fd9a0fed4c242a27`  
		Last Modified: Sat, 17 Aug 2024 06:33:14 GMT  
		Size: 154.5 MB (154503694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50846f3a5fca54082821717a4db25aa4a3390e5831aef8009a89fe11be735dc`  
		Last Modified: Sat, 17 Aug 2024 06:39:02 GMT  
		Size: 80.2 MB (80198444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a6f74b6c779ba710163511bd97a34f5af70a635e46421e6d51d67d469876e8`  
		Last Modified: Sat, 17 Aug 2024 06:39:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4930b8bc09e9c4bd63a75bc59a444277bc5273fd9e881c392240a8c703e2c79b`  
		Last Modified: Sat, 17 Aug 2024 06:39:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:745d20a73fceb0155adf0dc6a5ece3df3b667c60b7d32170e570a7602e776422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cddb0d7a0fb8999fb9044f99c94a2b304371f1ec0587eab1322470931297e7e`

```dockerfile
```

-	Layers:
	-	`sha256:22b63cf5ace49be23bf44dec23bc94290fc69c3671cbc77d4ce1ec32d277c795`  
		Last Modified: Sat, 17 Aug 2024 06:39:00 GMT  
		Size: 7.0 MB (7007175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f686023dbda61f7b1893185858c9b5d5f6b186193493ee61443f1300cfe4ae`  
		Last Modified: Sat, 17 Aug 2024 06:39:00 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json
