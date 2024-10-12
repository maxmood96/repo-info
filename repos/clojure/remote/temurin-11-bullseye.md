## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:d27793b9171c0fca11bdc098b4e006658a1d9ac8f348e1a99c61b5577ec7bb1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ede50fbe75bc7811726be14f1a5ec62cb95365d9dbf1418215e10b97cc4ea3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269965780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa55856e76ab2c89e27fbe807b32bb65c96bd5bd167c48886e31a14b82e84655`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982dca9ad462cc63098a78a315ac6767aca658a85763e11ea8d0b49bf481ded3`  
		Last Modified: Sat, 12 Oct 2024 00:53:56 GMT  
		Size: 145.5 MB (145549901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c6632f475f654d3cb26f24e3ea71d6521885e2dff211a6119d68e4d68bbb3`  
		Last Modified: Sat, 12 Oct 2024 00:53:55 GMT  
		Size: 69.3 MB (69333842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47d103f3155ab0bb95c110b217fd8fc4639d2ad7caf8643d1010036eb69a733`  
		Last Modified: Sat, 12 Oct 2024 00:53:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fc1b1244a4833badeb165a2837c5b5f1ad7476804a8a887a64ea69edba1dae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81ca06b22e0e456a199090e8f94c28b54e8bae424ac41feb11ffb920c204020`

```dockerfile
```

-	Layers:
	-	`sha256:adb47e1165a199c1435b559c2f1ea0a3cd7a13770c90d9013935dd0e816267a2`  
		Last Modified: Sat, 12 Oct 2024 00:53:53 GMT  
		Size: 7.2 MB (7210170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46346e4473650dc75cafa71ff0264e40f28062721c83beb860de03f06bd8afe`  
		Last Modified: Sat, 12 Oct 2024 00:53:52 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fbdcc9f0749357010a3205a9e8f970183fba4131cb23dec1d332854412c47162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265556491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc0ae81a1d7b7ced97167bc7c9a34863336464a66e0ec482f1682f0a394f14a`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7e0044899dfa730a974b795d6734e7657d3c5b47173312473825df3312bf51`  
		Last Modified: Sat, 12 Oct 2024 01:06:49 GMT  
		Size: 142.4 MB (142355074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dadc7dd9be4e3d2d86c7a93d83522c9bdcf2f3f1e14ff66c022ff7c833eba42`  
		Last Modified: Sat, 12 Oct 2024 01:11:02 GMT  
		Size: 69.5 MB (69466908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d391d0d69ee9887d0761c7986fd6d11ecba0ce2309b7230d714a30ad8334ab28`  
		Last Modified: Sat, 12 Oct 2024 01:10:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8f869cbd42b76528e54e716d37e4c1af8e575a796e71da56be27292ba8818135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31bdb9200b34d6cc4fd53b1b29d89cac634f4007fa14cc95e188fe728b28e868`

```dockerfile
```

-	Layers:
	-	`sha256:f62acea5a49816483d2901f6650e6f30997a4daec7549efb1e3614855602290b`  
		Last Modified: Sat, 12 Oct 2024 01:10:59 GMT  
		Size: 7.2 MB (7215892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d02bd716b23fce0e1240fcd05f2b175adfeeffe92e3e6ff4fa759ceea8df58df`  
		Last Modified: Sat, 12 Oct 2024 01:10:59 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json
