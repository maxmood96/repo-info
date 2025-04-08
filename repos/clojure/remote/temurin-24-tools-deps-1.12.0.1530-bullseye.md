## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:418e0e3ad2368cc3b09ade501610eae3f3747a53de616a9fa49da33303f059f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cd25db509e75605c145561732d4460fec06c24e608b338e5a6b6d7ff79ae247d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213093390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4507017a7b08ab6def4e2202a29b14c2ff47ed1f579310821841469a95c3efe`
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
	-	`sha256:4e0c55aa6f5cd2d63dad7193fe1b3f123a202967ed01e4635cb59f3ac85d2dd4`  
		Last Modified: Tue, 08 Apr 2025 01:36:58 GMT  
		Size: 89.9 MB (89949050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cbc5ce7d9091bfa9bbe23d920ff775c88a49587f1d1aaf75cff5f285f6b823`  
		Last Modified: Tue, 08 Apr 2025 01:36:58 GMT  
		Size: 69.4 MB (69394773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f04bff956d537a2bbe8ae7a168496be49cb68f4977b1141fd515f210ac98d65`  
		Last Modified: Tue, 08 Apr 2025 01:36:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5858eadf5daeec7fcaca37dd59cb238d867d8f8ae9531acea9fa3a906d6fef07`  
		Last Modified: Tue, 08 Apr 2025 01:36:56 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:40d6c241e6a58772da97bd581a948ada01b3cc27a91a71a3d0d19da8f6555e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359f837e64e30a1700e6e48b1bc56aa259d74b1db1050c40ed985a6d5db909d3`

```dockerfile
```

-	Layers:
	-	`sha256:11aabb52d80e5826c807dae0fc883c8d688d0cdcc9162b222aa98848614c1554`  
		Last Modified: Tue, 08 Apr 2025 01:36:57 GMT  
		Size: 7.2 MB (7157133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cadc2e06577955cccba9ab9edd5a6b386be20835c0d72e42b56ef0b6d96ccc49`  
		Last Modified: Tue, 08 Apr 2025 01:36:56 GMT  
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
