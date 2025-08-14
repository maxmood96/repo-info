## `clojure:temurin-24-bullseye`

```console
$ docker pull clojure@sha256:682d7fff31541f2e5649cae2a85d8234f65d8f03deb357147ed493fbbdc0957d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4bfb22ac49895f779ac8ee496c30d9e37764e23b272f3ee0cd50b1ddfa331089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213141360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30187dcbdcf4eea3215bf1dc78cd17daea18d74bc39d95b6a5f3f459e3f62d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dafa1158fbeed344c9f394670e0378c9b9877edc5d9d22b69fed6fd561db17f`  
		Last Modified: Thu, 14 Aug 2025 04:25:26 GMT  
		Size: 90.0 MB (89975231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d943e8aeb4ed66e454d4b80c9c057f76c515c01ff8a1ddd942fdd5fab4170f`  
		Last Modified: Thu, 14 Aug 2025 04:25:19 GMT  
		Size: 69.4 MB (69409744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae44d7e75446ac7853845e1008ee389e68b36460c82c2a1b2c61d4e314ee65eb`  
		Last Modified: Tue, 12 Aug 2025 21:44:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6825aacccb64f0e66de55c1fa7df8b5a0654287b95bfaf90edd6dddee51483c`  
		Last Modified: Tue, 12 Aug 2025 21:44:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0f0954828b8f211f0efb015d27ddbce669fc364c22400ae518e44e3571b559e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03719cd435f82486870248f4e39bc497f1b45385be58e7390952e3188d8fb39`

```dockerfile
```

-	Layers:
	-	`sha256:b7ab0f372344d5173a09cd85127371b2a08a3d71450f7b632f6eec3b159bcf0d`  
		Last Modified: Wed, 13 Aug 2025 00:39:59 GMT  
		Size: 7.3 MB (7346286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e43942fdf3760206530c30ce1d896647b828407f253b54fd308231cc67f98a`  
		Last Modified: Wed, 13 Aug 2025 00:39:59 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5085b1cf9b42b2f919304ff09f3f36787dbd31b1ac79bb678429f72d10e43ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210879524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4da1b2cf747aa6a32dc9d4340f6f89334404f12235b85b6c65cd628c1e4a68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b0eb14d028d7ca6493dad8f60f9a31500a52a8a65b8a88906409c93baccfe8`  
		Last Modified: Wed, 13 Aug 2025 14:41:57 GMT  
		Size: 89.1 MB (89092517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f4322c7ec53b21e64e2ae15cb22325e7b151487fcbd135106c3c1c17aa3a17`  
		Last Modified: Wed, 13 Aug 2025 14:47:05 GMT  
		Size: 69.5 MB (69537558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fd11373aa8fece23756ada1f06e2c4ea596bdc45218354bdf70fb918dab0b3`  
		Last Modified: Wed, 13 Aug 2025 14:47:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3edff215c8db51169dc8f1990cbc558728e72c4ae2b18f4844004aba08b3e7`  
		Last Modified: Wed, 13 Aug 2025 14:47:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e05c990c33425087112b6f2d0b2354d2bba04dc23c22364f1d0088dd8d6f0eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61700b03ba41af6fda4e2d6b0c82f9a7013ec5a7302bdae954f59bbaa624a0f`

```dockerfile
```

-	Layers:
	-	`sha256:adad46fd6f4bdb7170fdcdb33ee2c76c63b078c01a1668716756e85351729e16`  
		Last Modified: Wed, 13 Aug 2025 15:40:31 GMT  
		Size: 7.4 MB (7351382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b9ab6947e1363e5adf83bb01837332294a92b30a1e04917b0bd7f7587a5a472`  
		Last Modified: Wed, 13 Aug 2025 15:40:32 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
