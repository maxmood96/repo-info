## `clojure:temurin-22-bookworm`

```console
$ docker pull clojure@sha256:531eb9065e64e06f93a2d6f5faf23b6224d7ba71f8091db815e7c58dc9fd6f63
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
$ docker pull clojure@sha256:a03ef51b12383bd034c993cf1594cd4b2db73000d320151f76dced66e97cefa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284291645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e4eb9cf98a4169d38001f9fa1a5f3045bc6a6cf9d075010fa035501ae9327a`
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
	-	`sha256:50164e6b61db9274a9d5aca88ac93ce591c94597645a586ca6335fa78d9484e7`  
		Last Modified: Tue, 13 Aug 2024 06:44:33 GMT  
		Size: 154.5 MB (154503731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e039832acba72f823d7f411540aec06722bb1ef927e16ac8bca14fd799fe51a`  
		Last Modified: Tue, 13 Aug 2024 06:48:08 GMT  
		Size: 80.2 MB (80198284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49ae9b1b023c21d68caf8b69195c77af7c5e80e30a9542c1db2557585dcc949`  
		Last Modified: Tue, 13 Aug 2024 06:48:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbdb0701a16e1b7b0c47c483c4781cdefcf5c997b4d79e304942529ffb412ea`  
		Last Modified: Tue, 13 Aug 2024 06:48:06 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:18d3623b9f11ccdf761537ec79881fcbde20c4bcb235308f46ea082544c73f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad10b42e3df3755966e67a63b9b1c336a8c4bd60074629a2137cc3cad525199`

```dockerfile
```

-	Layers:
	-	`sha256:4e7e2f47ebe05f53bcd96ef4dbb39bb5a270e93b8d89e7f5011037bc23184b46`  
		Last Modified: Tue, 13 Aug 2024 06:48:06 GMT  
		Size: 7.0 MB (7007175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b21867df4a4b1e4134c5eeb1fc25462a724950d7631be328d9e9513e3b4364`  
		Last Modified: Tue, 13 Aug 2024 06:48:06 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json
