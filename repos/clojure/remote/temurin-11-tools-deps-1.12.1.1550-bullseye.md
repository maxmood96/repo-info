## `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:e6d8e28839d7bb30a62587566f78b709304f2b693482db8739f0865964079b3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:671c15f6b8df2e17fe50e1d2039598a17f08991963dc75d6f00a6fa02a4ce43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268800822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb08826b834bfaa848ba97e2c69b8811c186d7ec3bb85b140a149ee6f1bf59fe`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fafc410dbfc5c280bb256fe5797af0052ee6ac8ab95422ed486e79d7bb0608e`  
		Last Modified: Tue, 01 Jul 2025 02:38:59 GMT  
		Size: 145.6 MB (145635640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce673f94f27350fc77add0c022568d21858bbe135f184cf0fff99fe7a268cb74`  
		Last Modified: Tue, 01 Jul 2025 02:39:17 GMT  
		Size: 69.4 MB (69409717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd365c7406c903d388e11e2834238b5d95f943e8ec611463bd9db87f0238c9bc`  
		Last Modified: Tue, 01 Jul 2025 02:39:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d41e278a68feb0cd65d5bfbaa748e097fa927862f70de172df08a36092e78f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8a39be7e885181830439d97c58eccd2276f50fc2e28a34510d7f920cef0e0d`

```dockerfile
```

-	Layers:
	-	`sha256:7028d69a42fc6a143ea383b682ac0cc23fc9f8ea60d349fd0d1d817daa2e2e19`  
		Last Modified: Tue, 01 Jul 2025 06:35:24 GMT  
		Size: 7.4 MB (7415779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d24d5501c6700731d4d4bf9f6b7c679af78be33564abcb15bbf6eaa655de14`  
		Last Modified: Tue, 01 Jul 2025 06:35:25 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:58cb99e8b68cf5f31b2d86fdc879161fcba5611c117c9978bcf64e15ee0af27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264211435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e612e8f755845ca76e5b09af8059754027db5a5e0718076cfa7d9c82f1dab9e`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e68a0d15710888520eb4d4fb63dd03793367f39d9925dfa2caafd3398536222`  
		Last Modified: Sat, 14 Jun 2025 09:16:13 GMT  
		Size: 142.4 MB (142420681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e1c6b5ff3b35e6b7b2871ba3bbb5fc166ffcdce417df9585dcbdd7f7819cb7`  
		Last Modified: Wed, 11 Jun 2025 08:21:21 GMT  
		Size: 69.5 MB (69537807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa5e7aeb4900814de6bb3ded59773511215d8586235a3aac2a0466621191c7`  
		Last Modified: Wed, 11 Jun 2025 08:21:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:32c047d65f8866a6ff37b38dce925da8689e9c91dbc751488a6fec377c37a63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda4c0547193cc3595316f380964d7a332c44da7411773a4e536129d2e249c9d`

```dockerfile
```

-	Layers:
	-	`sha256:3e6dc14c38ca20eeff6118a90b566baaad14238fe37d54e3fce9becad029d531`  
		Last Modified: Wed, 11 Jun 2025 09:35:37 GMT  
		Size: 7.4 MB (7421496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0e40041ebdafbdacb8d4eeaf33c5843c381aa864549ed764d3a2b187ab5ea2c`  
		Last Modified: Wed, 11 Jun 2025 09:35:38 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
