## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:81769858b81dabb9ec398d61e5a36214044a169a93524d174c98e19842ffd4f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1994d75a2920ebb4616d14c14050af675dc11b7e69d27dbb7c339b5a853175ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227881683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6f665a93b954a2e4362d22efe857dde029d57a62b0e3127205fb8b9427668d`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d890f17d44f93043a29704338d04041f083f1ad2898ce42520ff03d9220e38b`  
		Last Modified: Tue, 12 Nov 2024 02:22:51 GMT  
		Size: 103.6 MB (103633891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a69af698628b57756636d2bbe655e1b4e873a8862cfffc820a2fb33e8dd932b`  
		Last Modified: Tue, 12 Nov 2024 02:22:50 GMT  
		Size: 69.1 MB (69138368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c2fd81349f9ded29ff2bfe2b4edc46b4d70b882016e404cbe9aa715c4e8b73`  
		Last Modified: Tue, 12 Nov 2024 02:22:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c489f94fc0b0eea287a7de84a03bed8318dcc8e65165d045015683d7e74bb2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8046819bad2d99a2b6dd8be332cee4c1999452d150becee246048f872faa99`

```dockerfile
```

-	Layers:
	-	`sha256:65548163013a6982ba1cf20b5b1432d282cd57232b2902ee83b5f8e4c2598146`  
		Last Modified: Tue, 12 Nov 2024 02:22:50 GMT  
		Size: 7.3 MB (7338040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:504c2423cae46804973a1f103fbda3ec9a7bd0223943ade8ec75544db762519e`  
		Last Modified: Tue, 12 Nov 2024 02:22:49 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e13ce9955199a9ac2013654c42f199b442a57427be9905df4a8dfbd5dffb5cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225783642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d232e136e736da246ca2cb69be38123f051717714adf58a70cfb95950fd55737`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41a217dfa452cf5f6f666760f99a72a32db30425e91706a2bb6cc5bf8304f4`  
		Last Modified: Wed, 13 Nov 2024 01:03:17 GMT  
		Size: 102.7 MB (102747718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c124a429ea8b244f08e082cf5c20a65226b195f89590e8d2d8fcd15f6235fa`  
		Last Modified: Wed, 13 Nov 2024 01:07:19 GMT  
		Size: 69.3 MB (69278210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d57891ff4ef5da1caf944209186b4ff09c4b16b7856f4d8a41c71463c22936`  
		Last Modified: Wed, 13 Nov 2024 01:07:17 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ded329c397b4ae5326ac948c0e48e74bb0a1844323fcffdea3c8849d1884977c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7358202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a99a52024e94f875e968ac5899fcd41ca74634466687740eb44e7d79b15ce4f`

```dockerfile
```

-	Layers:
	-	`sha256:4aa2b61baa8d0ce49fa7aebb882d4d9969356a27864c74fcb03dcf88af8097b6`  
		Last Modified: Wed, 13 Nov 2024 01:07:17 GMT  
		Size: 7.3 MB (7343842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c00ceb36c9aa5791044b23554fae9bc5fdbd8b541eae23b59931932dc8451bd`  
		Last Modified: Wed, 13 Nov 2024 01:07:17 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
