## `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:a4f886bb96a27d94165918fdd133768a6d4e8d89b08a89ccfd24f2182efc463b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1b25110f805bbaa1cbd4674042e84003835aad4d7ae44730a284dbf83ec32fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284795229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb71a63a7a60cf1976b153095e7937b07b2e67ca7e9aacef8ef893a8541ed97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:19:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:40 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:19:40 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:19:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:19:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:19:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:19:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c705e0ce2a2cff7397abd1f855a0dafed72c4354627c814537ff59bb0087d60`  
		Last Modified: Thu, 11 Jun 2026 01:20:17 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec818eee4ff5b20d7aeaf6caf81769646a19a674bdfa8a3d26bb57f5ef132f75`  
		Last Modified: Thu, 11 Jun 2026 01:20:14 GMT  
		Size: 78.1 MB (78125209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d8db5cb6e12840e453bdb9f07184a1e788a02102091c6c57fa2135ae8f48c9`  
		Last Modified: Thu, 11 Jun 2026 01:20:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47b45b6736af5a6ce059d5ee263fbf3245b7f65dc9557f5b05da3f4e4f9d794`  
		Last Modified: Thu, 11 Jun 2026 01:20:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b779abcb59133fd811dcf6aa9ffc78dc9565d2fe32cd744817ed948be07aa2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403607decf854ef4057235024e7c00a3a60da13dad14397fc5981c744d67da43`

```dockerfile
```

-	Layers:
	-	`sha256:c734e0af9ddf63b27de8b5fe215dfd2aa0055bb97fbb8f32949d9b444bc18682`  
		Last Modified: Thu, 11 Jun 2026 01:20:12 GMT  
		Size: 7.4 MB (7378670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5430d479463545d363243719dceacad734973dee2bdffb758c7fdca1275059b`  
		Last Modified: Thu, 11 Jun 2026 01:20:11 GMT  
		Size: 16.6 KB (16615 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9da41d0ba6ec3e927443a98a76b05ede17bbb5a1f285ed7dd48ef026dd93fe86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282980880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ad8183ba2b4d06a5b9d35013607f60850b7717ec9a746a5915ca35e53614f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:24:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:24:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:24:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:24:02 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:24:02 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:24:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:24:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:24:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:24:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:24:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ddfd84dbcb62a55872a3d72c0ca9bee58527571f27a9e0a75103edb879530a`  
		Last Modified: Thu, 11 Jun 2026 01:24:42 GMT  
		Size: 156.5 MB (156461227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0772c7051ff765e4cd756f640f6f6e48ffb257f643f6bd51056e92c33269f4`  
		Last Modified: Thu, 11 Jun 2026 01:24:40 GMT  
		Size: 78.1 MB (78129598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e7ffeefbfe480ad283905d3ee67898b293949da51f99bbb326e53188a2c875`  
		Last Modified: Thu, 11 Jun 2026 01:24:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb72d20bc649577304a93510dcbea93dc2a58d78cc1e58014e575a71b2292cd8`  
		Last Modified: Thu, 11 Jun 2026 01:24:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9f3cf83bc7715853f02ce19f534893d2390e892491ef4a9d9cd46e36560db612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2c1ea20017dd0cb960d9d6bdccc57b9eab134b84c6e68e58688ac5cd3341fe`

```dockerfile
```

-	Layers:
	-	`sha256:26a6d8124613cc27faa94236ab216c3ca82c4ed34ce29122b797f4e928df0113`  
		Last Modified: Thu, 11 Jun 2026 01:24:37 GMT  
		Size: 7.4 MB (7384457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99c83b04fcf97f0b80a3e0e71d731c5831e602889ed741623c69b93932b81c0`  
		Last Modified: Thu, 11 Jun 2026 01:24:36 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:914af2db636833b478006fab71d0609c271e8f17b1e32a94907d1d77ed20cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294649803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fe84eb0c92908eec8de09ef9097ac251e0ac7b7860ebc09f230bb4a7517a29`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:36:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:36:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:36:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:36:58 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:36:59 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:40:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:40:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:40:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:40:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:40:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce7fc17844961c443ec6ff9fc6852d7315d0c5de57330a5cd0dd3369a5a4e22`  
		Last Modified: Thu, 11 Jun 2026 09:38:13 GMT  
		Size: 158.3 MB (158343198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b5b997bb1a8620b64fee36d8c0da681ce78d4f0015ddf3f412e1bb73a6722b`  
		Last Modified: Thu, 11 Jun 2026 09:41:32 GMT  
		Size: 84.0 MB (83958897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2675af951ed93f9d5fdf32ab5a193f1c8fdd3c525abb3ec0de6d5a69c89bbe`  
		Last Modified: Thu, 11 Jun 2026 09:41:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bf508982b78f20fe4b74d262fe41e331ebaca0881a62a3e0bcd95e76bba9ef`  
		Last Modified: Thu, 11 Jun 2026 09:41:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a3f2dcb59c611d86cbfb5f000aa6811c64a091cc68fb93f2d9d823f98549a697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2e55ae1a505dbdf49418f3c63174321fa112ae956bb6a925928cd0c53fbec1`

```dockerfile
```

-	Layers:
	-	`sha256:b2f023eb1ca6ae41d246b54a49dd3af76cac5ec52f605676f06a503e2c92e871`  
		Last Modified: Thu, 11 Jun 2026 09:41:31 GMT  
		Size: 7.4 MB (7383898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf2ee8c5ccaa2bee24517b464d16598414ee0c59d401bdb8ee16d18a12f493c2`  
		Last Modified: Thu, 11 Jun 2026 09:41:30 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e3b862347c5dc338d89b0eb17b237ed6ab9b9ee112dc61ff7388eb52af163eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271479921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6358e1e6f6072b2ef2a809a19232e557ff9a716aa850b72bc07691b492f6f547`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:11:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:11:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:11:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:11:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:11:05 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:12:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:12:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:12:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:12:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:12:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315e35399e5d4547db2084583fbe80262cce5f385bc84081f625e7edec4d8b6b`  
		Last Modified: Thu, 11 Jun 2026 03:11:50 GMT  
		Size: 147.4 MB (147388354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b672f3ef2e9b5657b34620ac84ddca5dd7ff191dc54be29d0716ea56cb3c3495`  
		Last Modified: Thu, 11 Jun 2026 03:12:55 GMT  
		Size: 76.9 MB (76929029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f4b61944ae93c6d7d5b30fe0a66ac52f2993f8db4ed300e3bb96dfaf7cc80c`  
		Last Modified: Thu, 11 Jun 2026 03:12:53 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc12f60e224b78d2c8acb4ff0ff83fcb05bfc19288f0f633b907450cdd243c91`  
		Last Modified: Thu, 11 Jun 2026 03:12:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c9dfd46c6059dddac185f1664d847c3832a7a206361b80aa0324c7aa03cbf2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7e83bd21d78e05fff7b03343b0e45a67de98c143187eaee582ff8ad14ecf9b`

```dockerfile
```

-	Layers:
	-	`sha256:472a4102bf3a7bcb6b43ad3750c3637b86f45f77462b694982fd3a84fbc91b79`  
		Last Modified: Thu, 11 Jun 2026 03:12:54 GMT  
		Size: 7.4 MB (7369989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7022ad45fb65537e1d2d356ed10d787993ad3209dc3eafc2a73e58da2b2d64ed`  
		Last Modified: Thu, 11 Jun 2026 03:12:53 GMT  
		Size: 15.7 KB (15661 bytes)  
		MIME: application/vnd.in-toto+json
