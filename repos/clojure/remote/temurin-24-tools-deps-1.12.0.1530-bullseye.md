## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:200b1d027aaa07e3232133841e4c81e69a230210553be31c44fbad814ce88ad2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a6c19e7285e86def9ee8a041f6c51842aea2a215a04b2e552a51280575d2edbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213093556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6dfdd2e8e860c01d9b001082c3fb68a01147f0a0155fa11b4129e2d0ff3cb8`
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
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674a5641dde0518677faf529d9034a7eee4160a78d74b2a19e35942139b53312`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 89.9 MB (89949101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd16cb57fedc40a6156a9f1b989125a3463299276087498e9de75ceb63d40039`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 69.4 MB (69394887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae439077059886c72f26ab7f4a116a796e69d7bed0ee11a471e5e187497e08`  
		Last Modified: Wed, 09 Apr 2025 02:19:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df70c785cf2a18275ce525b235b04e68b2517a9cbdb1d58b7add12864de8ddd`  
		Last Modified: Wed, 09 Apr 2025 02:19:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:038d0239f0a89eaa6aed1309459cfd8eadd2dfc4993c4d3e52905c0f5951d5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cf4731f724eca632f9e17f4c50d65594fd77db04908a6a51df92f8eaf0f006`

```dockerfile
```

-	Layers:
	-	`sha256:7841aa8ae61dab2e6b0c5d9ca0a36d104852d4e20c45e1d0123a932d3faa7a64`  
		Last Modified: Wed, 09 Apr 2025 02:19:35 GMT  
		Size: 7.2 MB (7157133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4132e2e271ce897f40a2be86c9b7d4bd14907a22c61208d4838e2217ede228`  
		Last Modified: Wed, 09 Apr 2025 02:19:34 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6738ef688a24bb48a6b4e5da920d274841e05a80ac13a1ec76b39f42d55a34a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210877640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8b0437677828c9b653cbd641428bd0030b9dda17fcf9ad0d9e4a73be1b419f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a321861fd882958fec723f3eadfad5e1c97d33a7ca62e8dcf7929a2ee596db7`  
		Last Modified: Tue, 08 Apr 2025 11:38:48 GMT  
		Size: 89.1 MB (89092720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306a90b198181a78ff7c3cff70257745db34c8b57962c0af45a8f80bfcf5b162`  
		Last Modified: Tue, 08 Apr 2025 11:41:40 GMT  
		Size: 69.5 MB (69529655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e7d26b8100351209e8021da73666e9124fb89945fb9aa0c28347511a2b9ad7`  
		Last Modified: Tue, 08 Apr 2025 11:41:37 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634e5246504c7cf923b58017a4d3d8a15d496d9fe81515b1692c64ba8c57a27f`  
		Last Modified: Tue, 08 Apr 2025 11:41:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bcda99876573add9a445ce8fab8fab2a3a37727e2b5393afae872a849f05361b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb22fb302ce5d90146c60f34fcfeb402cf1b630dfb302535d050754f32c51e77`

```dockerfile
```

-	Layers:
	-	`sha256:b92807cf18c8427a5f75ee25fae21724c13122ee38246a606fd9de2b4a070185`  
		Last Modified: Tue, 08 Apr 2025 11:41:37 GMT  
		Size: 7.2 MB (7162229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a02f7f3cc6cb90833872af3adf74c9fda8a50f995d1aceda2006ec15904d3682`  
		Last Modified: Tue, 08 Apr 2025 11:41:37 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json
