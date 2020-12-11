## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:cc96f6817a7592c4ede7e8db7b9e2c55a79be5e6103f88728db5c595a39e24e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:fdf27ead951da5e692d8df31873ef42c82dc2a25c7f0b04176db521aa9d8a159
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23178969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821cc2b89a53d8e4ef0c213eef01cb4716de3fb45e5ac4c7c957e47040bf7c40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:51:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 11 Dec 2020 02:51:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 11 Dec 2020 06:11:31 GMT
ENV KAPACITOR_VERSION=1.5.7
# Fri, 11 Dec 2020 06:11:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 11 Dec 2020 06:11:37 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 11 Dec 2020 06:11:37 GMT
EXPOSE 9092
# Fri, 11 Dec 2020 06:11:37 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 11 Dec 2020 06:11:38 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 11 Dec 2020 06:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 06:11:38 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9624996f533f5dfa6054365968149298c1183a1202c16061de0fc5093ad633f`  
		Last Modified: Fri, 11 Dec 2020 02:53:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b714c102d667de25287e212434b418f887c3297d809db411374920f3d8b36201`  
		Last Modified: Fri, 11 Dec 2020 02:53:53 GMT  
		Size: 280.8 KB (280809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae04b5137f000abc8cac383898f3143e57a86644ae27042a5d9aec6291f5476`  
		Last Modified: Fri, 11 Dec 2020 06:12:27 GMT  
		Size: 20.1 MB (20100611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e670b986ae7565da2b6683b0fb385e75fc34e7cb1c37a19ec0921259b68731`  
		Last Modified: Fri, 11 Dec 2020 06:12:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b8fc4ea8a40ce61c1f6a6c0501b5787341c9e029ff64de22fbe0a97a55cd45`  
		Last Modified: Fri, 11 Dec 2020 06:12:20 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
