## `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm`

```console
$ docker pull clojure@sha256:8c4f6bfb3b024aa14dd737c2fed756ad03081c796a56f5d386be3536395f6087
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

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:61dfc02dd459f7e84671b14375e27bdf2f66e5e6b78f2ace8a46c51e38a74e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219595314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42d8937da432b393015478cdb12a7d9239403c466e2e21315709b39c5218dda`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aef6c1606a15fb1170cb41785713e043a98e1cc887aa9d56a517f2b0e515eda`  
		Last Modified: Tue, 16 Sep 2025 00:22:46 GMT  
		Size: 90.0 MB (89975165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ee150915ef7e87cac4d40dbb628a5d583c296f3f4ab410016c042ea25b17e`  
		Last Modified: Tue, 16 Sep 2025 00:22:40 GMT  
		Size: 81.1 MB (81138495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11d93b74ae97a279fa147942c27eea03d4d5341f01db8dfed3e518af5518034`  
		Last Modified: Mon, 15 Sep 2025 23:35:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6405c68dab60494e4b9888ec2623390eaffd4ff4bf264e179ea09663ecb9493`  
		Last Modified: Mon, 15 Sep 2025 23:35:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5ff3e48b906fe7436da91ba3b02731e08e56825b91c8ac2b963b9b1e508138b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89777581ede3f3db5dad686979f096bf7a3bdbf15846667c2e7cbeca5b9d28de`

```dockerfile
```

-	Layers:
	-	`sha256:d36e1956eb5318dd62cc06de9a0ee3bc153147f476e408eb85064334d2541e72`  
		Last Modified: Tue, 16 Sep 2025 00:44:25 GMT  
		Size: 7.3 MB (7326222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890ea725b4b4b024a684f1d439aafe7c6d02b0c9d243d2b259b5994f2be6e484`  
		Last Modified: Tue, 16 Sep 2025 00:44:26 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8a7838892f2e92aad18c792e55024ceed2c5fb05caa97eb7f1973e27093329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218478279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a3cce72f27919f6eb7791c007acc2622e02a979b3e6ab47a8be5126db58c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247135a1bf86492dc7b8e8130a2a36a0e799559edc08562d2d53d9ef59d20319`  
		Last Modified: Mon, 15 Sep 2025 23:29:08 GMT  
		Size: 89.1 MB (89092539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152f9faa2202a6bbad763544baf972bf514771ce410d4820b3861c6756c14d24`  
		Last Modified: Mon, 15 Sep 2025 23:29:06 GMT  
		Size: 81.0 MB (81025681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a10363f8a5f94c2971fe980721562da1e7f1110c8b51764b341c43ad31f67d6`  
		Last Modified: Mon, 15 Sep 2025 23:29:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bab6924ff7b74d1d2da56a4d24cc7004a05cef6d00855e9d38c29c715fd0d74`  
		Last Modified: Mon, 15 Sep 2025 23:29:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d853b703aee92b27fc641e0a270ad7cd92e88d4451c10dc1dbc98cebd923056e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1618f8ebd58bdf1bd0f3d8af786aa8b66ca175648f45752947b10b23e423612`

```dockerfile
```

-	Layers:
	-	`sha256:d0353b44f84f026ab80b218b12d26914959716e0067b24b80c9444743555e645`  
		Last Modified: Tue, 16 Sep 2025 00:44:32 GMT  
		Size: 7.3 MB (7332006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3a090cf8254527c7feb8932126eb719343db3374d4c7bfb95ad9fad8c5cde9`  
		Last Modified: Tue, 16 Sep 2025 00:44:33 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:736d825808b73dbc1a653de77ff86ce1f6a2a9c4f906cf7000fefacd8f5583ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229224765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c24f0aec7a20c30af344b4e472ed0ae6eb29824b057d952ff6e30b38c60aadf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bc2c5531e92a66c56c069ba18e43acfa10489de9a21e221411308710d253b3`  
		Last Modified: Tue, 09 Sep 2025 12:54:50 GMT  
		Size: 89.9 MB (89918192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03fb7e246eba2b6e5f52f44ead62140c104d40b98cffbac045ce2526471f89e`  
		Last Modified: Tue, 09 Sep 2025 13:02:47 GMT  
		Size: 87.0 MB (86978710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49969c71b5b03b6983c707905f23df55f9ad6637ac49f75d1dc7e6dc2292ed29`  
		Last Modified: Tue, 09 Sep 2025 13:52:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5091b871716661b3f52ee2ffa291832cb5815762fde219d303b585154b5b8b2f`  
		Last Modified: Tue, 09 Sep 2025 13:52:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a421dea58355f9796b13be09e4e6293e6de7517fe65383c8b1f7062c89ba8c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7349304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6ed9cf84181db5d4c85aef14b63673d3bec21e5ace2b7b32715ab4434aaa05`

```dockerfile
```

-	Layers:
	-	`sha256:27806ac296a0e6aa6f279351022c3170931bb18d52ca16eecacef9ba4915e606`  
		Last Modified: Tue, 09 Sep 2025 15:39:23 GMT  
		Size: 7.3 MB (7332746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3372ea7a574e9f1c911f30750f0ce8e84db31986dbe48705b91b068bd8980cf`  
		Last Modified: Tue, 09 Sep 2025 15:39:24 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:95f3a802788e6f575411d7662024033c46eefa9425fa038f8b793d5a07f71d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212316092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c82febe487f0931cede22cb3121da1e3d25de576fa69fb2bda421dafb53a11e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b4a24baa0c6ba5b1c6628d50d52ab7cf427dcdd1ea7e424e55b26086ccbbf6`  
		Last Modified: Tue, 09 Sep 2025 06:41:25 GMT  
		Size: 85.2 MB (85226398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692a7616fcb3ac4dbb031bfc7fecabd205f639120e5f9daa39a330bd677b009b`  
		Last Modified: Tue, 09 Sep 2025 19:07:35 GMT  
		Size: 80.0 MB (79951114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f1c3453e7503d1f2b397d98f8b1f1615c18fc6f6e7f4d2f60e80c8d9259a43`  
		Last Modified: Tue, 09 Sep 2025 06:43:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ebac423e69d21714330212b4a1bd3bde028644729d8cf482ae68069652ce2`  
		Last Modified: Tue, 09 Sep 2025 06:43:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:306f37d1a1c8735126a0d0db2204c368ca7de60c01cfa2809d8f47f71d2c7a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7335788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cfcaa1dd6382ce6b31ac6fb05b60b46c6adde2b90eb604339dc123c451f374`

```dockerfile
```

-	Layers:
	-	`sha256:194e868cdbbea6259f11a3890a7f98eb909e557b5c3370069b8fa3244677d162`  
		Last Modified: Tue, 09 Sep 2025 06:39:56 GMT  
		Size: 7.3 MB (7320089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368c9b50e1e1bc7bc8fff705afe2bd9498a057970abe5574a5aa57c0bdb84c1e`  
		Last Modified: Tue, 09 Sep 2025 06:39:57 GMT  
		Size: 15.7 KB (15699 bytes)  
		MIME: application/vnd.in-toto+json
