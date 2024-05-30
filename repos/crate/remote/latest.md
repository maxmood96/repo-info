## `crate:latest`

```console
$ docker pull crate@sha256:6c773239683d52aa6afdabc46d6d3587a99d6ca2866fbe0dfa1f1d57d3a669a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:f102522a7c1cbcde795e87fb4ce5ace234f9d522ca2301fd227990d02bca5d69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198583951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd2d72e8b1af3e7c607ef1a3edd6bc03bc9f6ed1bbadb7d9f2b80e8d7b70afd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 19:50:14 GMT
ADD file:3fdb1e1e084f9adfa9354cc0d55674aadefb914a2a647cf64108082e380046fa in / 
# Thu, 30 May 2024 19:50:15 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:35:00 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:35:06 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Thu, 30 May 2024 20:35:11 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:35:11 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:35:11 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:35:12 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:35:12 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:35:12 GMT
WORKDIR /data
# Thu, 30 May 2024 20:35:12 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:35:12 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:35:12 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:35:12 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Thu, 30 May 2024 20:35:13 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:35:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:35:13 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:5f50a3278457f7a74799b60cb44c68510152a5ae686ecab49052c4e5aba464e2`  
		Last Modified: Thu, 30 May 2024 19:50:50 GMT  
		Size: 68.6 MB (68578181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299c2cad3cedc44786f6cf66f874ef6d3aab3c6c246503881f59ba1b33eb11fe`  
		Last Modified: Thu, 30 May 2024 20:36:53 GMT  
		Size: 424.5 KB (424520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8777b9d136d07781af2e1c328496e3d744cd628712063953f1b537cf616fd0b5`  
		Last Modified: Thu, 30 May 2024 20:37:02 GMT  
		Size: 127.6 MB (127638719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebe7fb06631d4e6e173b631e8392cc91f21245e8e5c730da93a295b7aa25026`  
		Last Modified: Thu, 30 May 2024 20:36:51 GMT  
		Size: 1.9 MB (1940648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80be2b39b73ddc110624aee6c44c9907e8deca77e12af50d0e70d57b21a10dda`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac73a3d073b3944966e33f7502c769aeafad521d66f762c46340cfa2a6f95ed`  
		Last Modified: Thu, 30 May 2024 20:36:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b296e5312310c9c03e6481c9775945ae48bbb5239c03eba8ffc6284e4ed5bac1`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa16674af1872afd51b63ac0cf3c3cde2cd3e3452f22e8e30b1948c4b17659a`  
		Last Modified: Thu, 30 May 2024 20:36:50 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:baa09b3f8e9907d4a46b2efca21385f1fad66285acfa4c72cd647ab1f5da84fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.0 MB (197015007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121024ee810b16ad5641246032d1bbc089f915f6a4c0af24b7dfd53766c97254`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Thu, 30 May 2024 20:31:20 GMT
ADD file:a880b559ba3dfc6070e73e3f70f23f5c0dc7d6887ba60c6c113f3bd16d0e14a7 in / 
# Thu, 30 May 2024 20:31:21 GMT
CMD ["/bin/bash"]
# Thu, 30 May 2024 20:48:24 GMT
RUN dnf install --nodocs --assumeyes gzip python3 shadow-utils tar     && dnf clean all     && rm -rf /var/cache/yum
# Thu, 30 May 2024 20:48:38 GMT
RUN groupadd crate     && useradd -u 1000 -g crate -d /crate crate     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-5.7.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-5.7.1.tar.gz.asc crate-5.7.1.tar.gz     && rm -rf "$GNUPGHOME" crate-5.7.1.tar.gz.asc     && tar -xf crate-5.7.1.tar.gz -C /crate --strip-components=1     && rm crate-5.7.1.tar.gz
# Thu, 30 May 2024 20:48:41 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.31.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.31.2.asc crash_standalone_0.31.2     && rm -rf "$GNUPGHOME" crash_standalone_0.31.2.asc     && mv crash_standalone_0.31.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Thu, 30 May 2024 20:48:41 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 20:48:41 GMT
ENV CRATE_HEAP_SIZE=512M
# Thu, 30 May 2024 20:48:42 GMT
RUN mkdir -p /data/data /data/log
# Thu, 30 May 2024 20:48:42 GMT
VOLUME [/data]
# Thu, 30 May 2024 20:48:42 GMT
WORKDIR /data
# Thu, 30 May 2024 20:48:42 GMT
EXPOSE 4200 4300 5432
# Thu, 30 May 2024 20:48:42 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Thu, 30 May 2024 20:48:42 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Thu, 30 May 2024 20:48:42 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2024-05-02T14:35:43.432591 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database that handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=5.7.1
# Thu, 30 May 2024 20:48:43 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Thu, 30 May 2024 20:48:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 May 2024 20:48:43 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:45508cd4bd17b58663654833a353dbd294c4db29333f10c1d263536b15decf92`  
		Last Modified: Thu, 30 May 2024 20:31:51 GMT  
		Size: 67.5 MB (67499004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ba7699aeedd0aefc965b5899df0d58922120ca6f23502b6b3e3c6ab91a6fe6`  
		Last Modified: Thu, 30 May 2024 20:50:12 GMT  
		Size: 423.3 KB (423292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce1cc4c6bf1087c8c8d1cfbeb622742b1a8c0d642772684a4e43f4868064a23`  
		Last Modified: Thu, 30 May 2024 20:50:20 GMT  
		Size: 127.2 MB (127150172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dddb0706b704f087d004f781f3edc3b28ee0366060bb6a60bb3e25bd4e3a945`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 1.9 MB (1940658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddd8cac97fe9d05b6fd59dc7e2a91ec99ae6fb1b0f3bc55e6fe5aeee71f129a`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75345bad7e502e81e171377de774903d7a0f4c02c59339eec0cc01cd25ba4106`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c6e807eecfa87edaf6d9dab165764072012366d77cdd18b92d63b31a58addc`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519b28701486bbe025e0c77aefc4dc9f06feba8cf4d884c5ac5bafbdec472daa`  
		Last Modified: Thu, 30 May 2024 20:50:10 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
