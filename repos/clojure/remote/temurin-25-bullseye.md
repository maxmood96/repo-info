## `clojure:temurin-25-bullseye`

```console
$ docker pull clojure@sha256:89d5f6ade7f0a24fdb66caeb91d4f1a0cd6c7679c2ef1dca56cb7ed4c98b0c48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9fe4782b3da8c9eaa37d28c8f8bb84c051de0d77cd7e78a8ce8301dc7d6da889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215936304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00985e03b5450e44afe644288afd293350d84c974aff7408089f703486106d65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:28:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:28:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:28:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:28:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:28:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:28:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:28:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:28:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:28:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a8c09278cae48ec6d5716b07a8c870273f15901c5b4bbf8dbbfe910ac69b42`  
		Last Modified: Fri, 08 May 2026 00:29:02 GMT  
		Size: 92.6 MB (92574614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2530076a7ac632762609b29d77fad55171f66dc4dd00e831750eec907d6a3366`  
		Last Modified: Fri, 08 May 2026 00:29:01 GMT  
		Size: 69.6 MB (69597498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0744fc1e422b282d7650ba4fe7d7831899cfdafb64b09a89901d69d02a31748a`  
		Last Modified: Fri, 08 May 2026 00:28:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3ea5395e70c302ecce40ae51c6bc01726115b6ffe5822ebf141c357ba85083`  
		Last Modified: Fri, 08 May 2026 00:28:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:faa2103e17ef5b07b8cb847b28385602abf8382d4ba69cd503d3ad269ade78dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b5b97fe27490a2beb638331ee1b0a5743bed010e4eb85fb92bd7711c2f753b`

```dockerfile
```

-	Layers:
	-	`sha256:5d7c55e77de34292a063abf6d8ff1f7c0b63773cab5b103f715ad77c6e71c58d`  
		Last Modified: Fri, 08 May 2026 00:28:59 GMT  
		Size: 7.4 MB (7376350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897acf732535553da926cac9efc4624f702f91cdffeed5c84baa19eadfc767f3`  
		Last Modified: Fri, 08 May 2026 00:28:58 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6e967fecc52877b38f03dea72fca4f2f9a138a06b24860af04b24eb37a3a6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213534815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70750c5529a79450b4487b9b0ab302835fe11c411087386d79ee361c8d6d037`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:27:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:54 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5344866c8ac687a28040c00d8bd15d6f6eb85e6470fbf5064a9c0f10e49391bb`  
		Last Modified: Fri, 08 May 2026 00:28:15 GMT  
		Size: 91.5 MB (91542292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081bd10db25731ef1df7ac017c96abf26f3af8067175f335074c4815d985b153`  
		Last Modified: Fri, 08 May 2026 00:28:15 GMT  
		Size: 69.7 MB (69738477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f6bfdb23ee1d9f987144a173c268e085a052dbfbb315f4fe9d510e0775718`  
		Last Modified: Fri, 08 May 2026 00:28:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8f9035b9b17ee934ae7716989e58d4f6749111b2014806d7f9d4c1c8a2427a`  
		Last Modified: Fri, 08 May 2026 00:28:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c8f0423329b82c8dcba0dd782a717789cfec63e3797256b0e5d97af344a51991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071f23410dce57bdef6bf996fb631ce9a52aa4fea0f176fb1159be5f47825319`

```dockerfile
```

-	Layers:
	-	`sha256:516a6877d7e855a505f6e0272b5ac27c76fcc21137ccfedd2e419a5c8f3e6013`  
		Last Modified: Fri, 08 May 2026 00:28:13 GMT  
		Size: 7.4 MB (7381470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7128f643edbca1a06be66f9a87a136c522e9872d62cbbb7c889a9efa6e43c122`  
		Last Modified: Fri, 08 May 2026 00:28:13 GMT  
		Size: 16.7 KB (16743 bytes)  
		MIME: application/vnd.in-toto+json
