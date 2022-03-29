## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:f4f6fa974920811818dfb6c270d59bbe5d5bade68b0be74684cd994e79af8c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ef4cd3408c73d477551dfb72aaae2abdeed0b9b9a08d851bfa122561f91bdbe2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22786692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7596cd4f4cf4a22ac894e20298bb8b808de42e832647b9f14d53b8f9f23eccf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 05:59:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 29 Mar 2022 05:59:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 29 Mar 2022 06:00:53 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 29 Mar 2022 06:00:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 29 Mar 2022 06:00:59 GMT
EXPOSE 8888
# Tue, 29 Mar 2022 06:00:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 29 Mar 2022 06:00:59 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 29 Mar 2022 06:00:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Mar 2022 06:00:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8e4488850ad3e08f0aba8d339de3abde1e79494ff7d9a00067fa8b08eed46`  
		Last Modified: Tue, 29 Mar 2022 06:01:38 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f25991090eec670a7642f167cf12c22992033088ab88cc13dd27f5d7b50aada`  
		Last Modified: Tue, 29 Mar 2022 06:01:36 GMT  
		Size: 271.7 KB (271672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaaa6fcac2260ec607ed995de50d7d5ae598edbea49cf4b31303459a61b14a9`  
		Last Modified: Tue, 29 Mar 2022 06:03:02 GMT  
		Size: 19.7 MB (19672108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1248964caea31424a9c33d7e3295221dddf0cfa49827d784f1042f9ef3b88fe2`  
		Last Modified: Tue, 29 Mar 2022 06:02:59 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c4c042f5251a173f8cc6bcef3590725b41eea4cdc97212885e03f5494638db`  
		Last Modified: Tue, 29 Mar 2022 06:03:00 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4692a723f66a42998f49e22f718968845f26d3ed54349b437f08602d75640477`  
		Last Modified: Tue, 29 Mar 2022 06:02:59 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
