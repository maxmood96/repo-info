## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f2d31617dbfe20b28a7062da2d039c5b442785385ebf71ea1e2ff65e2d5b8986
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:201b7c950e8d06dc7e2769005e9e1588928b03f4013e1cf1f506969f83713cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289543514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5109248d140e77a18b45e64eacdabb3164242b6f08285a2c1ea7d5b615096ab9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba7b5d8836ed8bb5c769cce378fa636d1483d73ce9a4ed9d3de7ed704d44d9c`  
		Last Modified: Tue, 12 Nov 2024 02:50:21 GMT  
		Size: 165.3 MB (165295097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85d1ba1637d6bb6338df5ae09bc153086d8451a79d8adb2bd73ed13b2d2cb50`  
		Last Modified: Tue, 12 Nov 2024 02:50:20 GMT  
		Size: 69.1 MB (69138597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e29e14a0082fb730ca0822ab659670ff066ab4b6fcfe5499b7893a2ce2fc9`  
		Last Modified: Tue, 12 Nov 2024 02:50:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0c37d56e940bf005fa5bf84122202323d6b55a416903ff82c3cc6bfbba304`  
		Last Modified: Tue, 12 Nov 2024 02:50:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5232debdea01d460a733495b2880abeb45fd5108db5e2f8a0059277ab6828ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd0a7de7e97ad318755903e17d69adb72bc89c6e987ba1ffcfa53c6799fc3a9`

```dockerfile
```

-	Layers:
	-	`sha256:7587080e9cda2107d3e3f17bfb7898b13e8203662549d9e90539ef6009f2f946`  
		Last Modified: Tue, 12 Nov 2024 02:50:19 GMT  
		Size: 7.2 MB (7220883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601ad44f3423715437f3955d1ea252ac1cdeeb9b955ac7e0ee8c4ab582f6f23f`  
		Last Modified: Tue, 12 Nov 2024 02:50:18 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2eb6f7a9900c50469de03af44140d5a503602b05150240c356f09fb913c87203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286316906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f664232400888c43ffdfb3d3fac23dea43c152dbe48be7c76fa4e1c87613f531`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acf1cb36b535060f6d0d7ed38f20da6ba6c0f57f682cf5fff1a08e2820f3ac0`  
		Last Modified: Wed, 13 Nov 2024 01:35:51 GMT  
		Size: 163.3 MB (163281795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb808a6ffc3555cb29ce75cd0d728dd914d9e4a97a5e4bcd8ac05e9229055542`  
		Last Modified: Wed, 13 Nov 2024 01:39:47 GMT  
		Size: 69.3 MB (69277005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1aed257d6f2fa4d61ed9ee7ea526769c5d977a40d7c97b57b10a8d2dd7e1ee2`  
		Last Modified: Wed, 13 Nov 2024 01:39:45 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d1f3fe4c41ec835b8a7c4b195cd0a58fcb7d3acff0e14c05ea872aef6b1dda`  
		Last Modified: Wed, 13 Nov 2024 01:39:45 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:48ca210ec8a052e643e8b871fb78959ab930c24fce7b057193c1685375199225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce939f873d53c3ecf339c61291981b04a88a2e3a24e74a2b94936e46b9f9ae`

```dockerfile
```

-	Layers:
	-	`sha256:61b044b5960cf3f68d56ae8dfd06fe249f34a970dabc23a475b329b2a33021d1`  
		Last Modified: Wed, 13 Nov 2024 01:39:45 GMT  
		Size: 7.2 MB (7225364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc6a7ba6b1347b8c30bb33925df0810257e8e5417fcbf3578c69a1a024a39ca9`  
		Last Modified: Wed, 13 Nov 2024 01:39:45 GMT  
		Size: 15.1 KB (15138 bytes)  
		MIME: application/vnd.in-toto+json
