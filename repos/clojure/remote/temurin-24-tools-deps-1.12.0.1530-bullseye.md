## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:149ed08a26ac9a7c98ce29c63558fac9116cf6439253fe470a3987b5af785017
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
$ docker pull clojure@sha256:3dbc5a5728945491a1317d19b79567a2b9b9392d88e782da37bd1b8a0d8887b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210666630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cb2ff78c25a91cb5a1167cc9a10abbed3590894042fba6c3d9416b8dbd2ebf`
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
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cff61800d77fea8ceca86197d0088a545723471fc54b8d8f0c4585f35410dd`  
		Last Modified: Thu, 27 Mar 2025 17:55:17 GMT  
		Size: 89.1 MB (89092706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f12c4fe3996f585212279472c4932a72c8f0445af43b72391e61e4616f5a53`  
		Last Modified: Thu, 27 Mar 2025 18:00:17 GMT  
		Size: 69.3 MB (69324491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee96c4dd30698f263f5a2e145c1ce8845223f09f2ba1241d2480432fd168779`  
		Last Modified: Thu, 27 Mar 2025 18:00:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce0e8e187e9966521202f8e09f822719b18b1f778e7d30bac5723cf992d4698`  
		Last Modified: Thu, 27 Mar 2025 18:00:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:debda77c57f5f7b3952305ad3a5eb23a1188a67b3abc41ae7b5636ddceeb9ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad947b762e777059a7aa9b2df2e2c7a8946f928632d0c17a6803f7981255760e`

```dockerfile
```

-	Layers:
	-	`sha256:34cdd44bfe00f1d62decd7c70ef30e048724de318fd26df29f32dcc855b014fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:15 GMT  
		Size: 7.2 MB (7160283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81402ce84e9fa14efdd8cefa74340bf7017a8d6e50d9bb11c522b88c7558cdfc`  
		Last Modified: Thu, 27 Mar 2025 18:00:14 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
