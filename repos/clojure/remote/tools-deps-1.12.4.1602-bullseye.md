## `clojure:tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:d319790015db2bf0be99e340d8c057fd7ee66b0131e29f20579677b4b842b659
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f66bed771d2a44fa40971b3c9352e07d5966229c23ec82a9d4cfeb609fedab5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215555276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f902693eba9e1c2c7f829ef3100253385ab3b303a294b68506e5967be0c2d1bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:46:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:46:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:46:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:46:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:46:04 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:46:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:46:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:46:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:46:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:46:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5bc37637d859d8a4c263e4f5b9eac7446cfa89d06a37e33dba8794ac106951`  
		Last Modified: Tue, 17 Feb 2026 21:46:41 GMT  
		Size: 92.3 MB (92256276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df80d7bf709fb52f27b03b74a6b72558c2a1f258fc64fda7524eb216c3a4cd5d`  
		Last Modified: Tue, 17 Feb 2026 21:46:40 GMT  
		Size: 69.5 MB (69541697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e37469b27d47085ee6e763da0e1e43c634322d38a1c162c2fedc3d822e6772`  
		Last Modified: Tue, 17 Feb 2026 21:46:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dcac14afb9d243a10b245f54033c927e5b646398a9efb04ad745caeb6e4764`  
		Last Modified: Tue, 17 Feb 2026 21:46:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9bddf9915acbc454f9076bb6837f0c47681c00584cf500ec940b478e4365c6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da01b009491cca7b4eb41b7bbe02f9597f34e7506d85ff4e58b3f04dfc16f14`

```dockerfile
```

-	Layers:
	-	`sha256:f34d181f9ce37ae90403c41b98944432c143e9c401e34d837f6101d61a63c2ac`  
		Last Modified: Tue, 17 Feb 2026 21:46:38 GMT  
		Size: 7.4 MB (7365794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55e86cb53245e86a8eb3f640adbfddd2ac4cb2bfb664c3cddd679040a78b8b99`  
		Last Modified: Tue, 17 Feb 2026 21:46:38 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:874ab7c2287043da8b4f2d8f37b67d8a4ba538e53de9cd3613f72044ed436636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213241266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7014f8b838f8d86f5d6cc563c4a12ee156b763fec152e62049c292aaecb332`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:45:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:53 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:45:53 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:46:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:46:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:46:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:46:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:46:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa78582e646a7f88fbd13b85074ba388d0a84ed5ebc961ecf48441d54c66f2e`  
		Last Modified: Tue, 17 Feb 2026 21:46:31 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772bb9df01729ff5b76f3ffc6ba7d827707f660f4827944aaec1812fb437241b`  
		Last Modified: Tue, 17 Feb 2026 21:46:31 GMT  
		Size: 69.7 MB (69693630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390da65ce491f6a164e9ae1026c86ff4f81905b504912a262eb926e148e6386e`  
		Last Modified: Tue, 17 Feb 2026 21:46:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789a8354ac4c1b7f6111c3cf50ebfc7c43e30ae26075c5e7b2867c905c4fc846`  
		Last Modified: Tue, 17 Feb 2026 21:46:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:adc84b84c905bab4a9835ea7ee41e6879bf1d926c8faf94f51307394e8de0140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873238449ddb22f4f49e27695d4d965c026ed7712ba5a32b558d302df0b414c4`

```dockerfile
```

-	Layers:
	-	`sha256:ec5cb821aa800e3e6bbd4083b873db244f15fca777e330079f9a3a695fa3625d`  
		Last Modified: Tue, 17 Feb 2026 21:46:28 GMT  
		Size: 7.4 MB (7370914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d403b04f35fe8cf3792ccefe09b57823cef3e16ce10f005a09bda5e931ddb8a2`  
		Last Modified: Tue, 17 Feb 2026 21:46:27 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
