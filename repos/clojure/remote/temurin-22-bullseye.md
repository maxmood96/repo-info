## `clojure:temurin-22-bullseye`

```console
$ docker pull clojure@sha256:90dc129c066dab2660d9651dbe71a9e95540d17af392dfc401404c07bd1b5469
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:772e30bd1145f559dfd8e82362f8411a9bb12dbc8ec96c29aa332aa0e417bd0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280529558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a98675ae9a7d5704b5fef03407b9dad7704fd8f323d340d3a72271d3d88f639`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a488068388cc21bd8825b86669ca3f4e6ed4e439cfcab88ba3a6d675026dc0ff`  
		Last Modified: Tue, 13 Aug 2024 01:11:36 GMT  
		Size: 156.5 MB (156481579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8c0d428c2eef67a74d602c739277c4aeee68a6eca55b8c7e2e8cd1618d5218`  
		Last Modified: Tue, 13 Aug 2024 01:11:36 GMT  
		Size: 69.0 MB (68962265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7437ea84afdc502b8f2dc4ee2236c6557f54211116d9d224acf67568a2b42b`  
		Last Modified: Tue, 13 Aug 2024 01:11:34 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f86e7d83f077aed87355ce48438353566b23c750115f1c9b610e02de1ac2e0`  
		Last Modified: Tue, 13 Aug 2024 01:11:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:23aae9be4cf6615ea6a2bc079013fa71b45466047e49bc003321232ceee9aa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77f1a8e4c5110e93af90e2332ab142b34daddfaa66664a193553ab5588849d6`

```dockerfile
```

-	Layers:
	-	`sha256:709c8c619880a3a270ce6e0bf0fc7e591b95ff6c77077e9335e7a058f2c148c1`  
		Last Modified: Tue, 13 Aug 2024 01:11:35 GMT  
		Size: 7.0 MB (7040338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:708589fedf0f6eb9d088305106c6d82097843442000ff5bcb0f0e452e74ed97e`  
		Last Modified: Tue, 13 Aug 2024 01:11:34 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f7bd85544afc6e4f4019187bfb64f1857c7d2790de2d4a372496068f2af5b4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277327109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8622c60349d03eb7be12af2a55424ecd03f20b50323111600912ff388c20b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
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
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b26f305860c4ff586a0338632919bd31b49a3b9bb89c8ebda5d6c0f4a1b3e7`  
		Last Modified: Thu, 25 Jul 2024 21:29:10 GMT  
		Size: 154.5 MB (154503721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d485530475b8e75bebf9e9da5e50d96c727a1ca063198fb04445f08b892ab653`  
		Last Modified: Wed, 07 Aug 2024 20:18:41 GMT  
		Size: 69.1 MB (69092358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93e31023e53b3d09ab278fd5a7adefefb9fe039be381d830693cd66b21244a5`  
		Last Modified: Wed, 07 Aug 2024 20:18:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9a4a97a4122a2c27d52eb14c1ce85a874d044676c5d77fdc8a349bb5ef9b1c`  
		Last Modified: Wed, 07 Aug 2024 20:18:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c17a5afa3ae4593476b0c6de27626617155ef8ad37a147b5042feb1c704afab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b7ebd980dd60798c478b4c5b118322f77272d63ec3dcf0281525a02e429fed`

```dockerfile
```

-	Layers:
	-	`sha256:38505078333bd0b53880c0c41b7a0f7165000688c63a4c1d37a26ed08869d562`  
		Last Modified: Wed, 07 Aug 2024 20:18:40 GMT  
		Size: 7.0 MB (7046060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3677ddfea6240e64518715d88d055d4f9cc02b461f08a25ba3f4f6720e4d82cc`  
		Last Modified: Wed, 07 Aug 2024 20:18:39 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
