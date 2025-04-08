## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:184a14ab40ae137fcca957be98f6d8a1f4ddbdea60514654c72563867147f20a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c3dece1d213e327e44890cffde7e5a9bac0cb391dba6793aff537a8a2e7ce6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179200288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c07941276eb6a7ae03aa1598e824044c88abe0e17c56b310e1a43e8c780cf61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63eb247c3c702339b2f368f5def817eeb52fe9335b5c7178fe1b0b9379133c83`  
		Last Modified: Tue, 08 Apr 2025 01:37:56 GMT  
		Size: 89.9 MB (89949037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d71fb680be5bdfcd4ee649b0ded7f42ff262a69ce61cd1a75bb653e659c0e8`  
		Last Modified: Tue, 08 Apr 2025 01:37:55 GMT  
		Size: 59.0 MB (58992794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f59c553835889c1bd039630a67dece6f0ecb407ca61f1c36489f63cc141da`  
		Last Modified: Tue, 08 Apr 2025 01:37:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30c051faa60d3cbc5b502a6b78f0232e8726a57001b616a46b17ccc54bfb6e2`  
		Last Modified: Tue, 08 Apr 2025 01:37:54 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8f17f60e3c8d6860e061b6b4e702279ef653f7941ee4f97cca2cce7b39197fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e423dc346d1ded5ca9cc0264e5b32314d75c5909143083d735913a328369c6d`

```dockerfile
```

-	Layers:
	-	`sha256:0f51788af19ad145a74cb1640b5477d306aeaf08f500bcd56fba3c33c6aed642`  
		Last Modified: Tue, 08 Apr 2025 01:37:55 GMT  
		Size: 5.1 MB (5069645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3551adbc0876299599dfbedc1e0e99a4530b2a4097f8e65911b4a68c4e32966e`  
		Last Modified: Tue, 08 Apr 2025 01:37:54 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ec648f5963d164ab9d3f2385c23957a4639d452c88866d990fcf507553c0d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176761150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522f1a24235de67e49a60fe0a4d35d16be852934de9a21ea5f51fb0c911f5ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810ff949c882dc88620936ab3b019fbb2b39d872539a484496b86f21d29abbdc`  
		Last Modified: Thu, 27 Mar 2025 17:56:15 GMT  
		Size: 89.1 MB (89092702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f63dc4f9f6ea1b454e32d67dc99c67da24568c23189ba5d91d462a8f421b1`  
		Last Modified: Thu, 27 Mar 2025 18:01:08 GMT  
		Size: 58.9 MB (58921484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5913ea595c019b2d096851a0ccd9096767d90dc90332dd5d2c3586edd45fdf51`  
		Last Modified: Thu, 27 Mar 2025 18:01:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f2dc6cfd6ab32b087d4b35dc9921e3bdbcc4f3a03f2b1e1b96a4a8cafbafa1`  
		Last Modified: Thu, 27 Mar 2025 18:01:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ffdb5b2cace1fb5d505fd265d3b43ea49d909809c05170bb4493d011ab8912b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabe41a4ec7494357483dc668279c7b989dbd870e5cd768ea360a18e2bfb3e56`

```dockerfile
```

-	Layers:
	-	`sha256:1cba9086828c3d57f5104ffe266380b8b822d3060da232dd47a0f670ad587509`  
		Last Modified: Thu, 27 Mar 2025 18:01:06 GMT  
		Size: 5.1 MB (5073428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf3fb1cfaca38fe9661ba04000dbfdc3dd191626136e9ccfbe13a4809a306649`  
		Last Modified: Thu, 27 Mar 2025 18:01:06 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
