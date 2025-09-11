## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:609480c12b390741c89135edc31b140edc7bd100228b67ca38437009c5c40aed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f9db43f754f4aba4a640d4abc91914d8345295b7afc3389767a4324087e0887a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281117733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7065fc8a22f75b82df9cb5c20874a495ef243823b8a9ce25c1623d446878e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be4a2e3fd56d9c5737a9d1e95716c81030d93f4e219a52e34b167744b933e48`  
		Last Modified: Tue, 09 Sep 2025 13:48:28 GMT  
		Size: 157.8 MB (157804766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a23eb0d0840ee397ff9154aecd4cbc7c1b7ac7bf62f81ccf12db00dc560928`  
		Last Modified: Tue, 09 Sep 2025 13:48:23 GMT  
		Size: 69.6 MB (69556532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232a39b98cbe0950803278ae6fd7d5ed333f64337faf53ae81959d4669dce9a8`  
		Last Modified: Mon, 08 Sep 2025 22:27:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72e3f54844eeee637659548e9aab795a42ca8d4d8d15dfdc1f83b702ba4ce2d`  
		Last Modified: Mon, 08 Sep 2025 22:27:34 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7311c07e174fe3c4c8813cc3725696ff28b50bef6ebcf14ced9927fd84d0f0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ce1f93d113fa57d34835c13b778e763da8a75906e187fc15a2a8a68da68f2a`

```dockerfile
```

-	Layers:
	-	`sha256:fa7901cb1f87716a5761e03ffb84265460ddf5ed9d8f1f821160d3b8a92b40cd`  
		Last Modified: Tue, 09 Sep 2025 00:39:52 GMT  
		Size: 7.4 MB (7399445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632c91ce092e8ed96d0b47261a7e575d33c4c354442a77302c88b61d25cafe8b`  
		Last Modified: Tue, 09 Sep 2025 00:39:53 GMT  
		Size: 16.5 KB (16496 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:502d56512dae592e0fdddc462f768dbfbf3869f68514fd78c3476ce3baf0aff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278014439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1488c8024668993b10ba0503437346fe97cfeb2da6f67a9685dc591f4dbb8299`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdfde2bfc8ccb26556cd27b1b6da296de706e7d6e513c07225d3fd441d1a80e`  
		Last Modified: Thu, 11 Sep 2025 09:33:14 GMT  
		Size: 156.1 MB (156081209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9d9c1e0d8f0f251d0de5479e877b9119b27537b12ce52f0ef2ef7e65ce48bc`  
		Last Modified: Thu, 11 Sep 2025 09:33:13 GMT  
		Size: 69.7 MB (69683821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404ee37a00265269f232aa7a8634a3aaa771a76aea7ace13bf1d63012d74a97b`  
		Last Modified: Tue, 09 Sep 2025 01:28:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb84eb31273959ba9b494abd0878ae13ca06d8005afa04b51a59c14f04dc3e2`  
		Last Modified: Tue, 09 Sep 2025 01:28:56 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e936526be89149281de9178d7ba08153207c48f6c85a729468be7fbdea0e7b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2571585d41328ac22611700cbf59bf508d4603246d3d02e2d257d82fbb868afe`

```dockerfile
```

-	Layers:
	-	`sha256:5508b08c917c35ae901fa8d4112170b2a909605024fb8a3fd8ee45bc4453f2a1`  
		Last Modified: Tue, 09 Sep 2025 03:39:39 GMT  
		Size: 7.4 MB (7404568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e7c83322b19bef5ff65ca29d80c3d8900024642cd8885a723406d6ff31a59e`  
		Last Modified: Tue, 09 Sep 2025 03:39:40 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
