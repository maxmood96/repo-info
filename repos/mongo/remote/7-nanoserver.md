## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:35d75da7b04f6ce6c1703471ee750b7059316be3b4b3b9bfcbb9e2ed68178a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull mongo@sha256:6aa9c4eb90bf414eb35fcbc253727a71f353abc8acbcc371ba85b77b491f7db4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **743.9 MB (743926041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936360cc692403ba9a1a802c5ef8a4c54de4e919d53b7da5bd212f07803a8245`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:15:41 GMT
SHELL [cmd /S /C]
# Tue, 09 Dec 2025 21:15:41 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:15:43 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 09 Dec 2025 21:15:43 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:15:44 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Tue, 09 Dec 2025 21:15:44 GMT
ENV MONGO_VERSION=7.0.26
# Tue, 09 Dec 2025 21:16:15 GMT
COPY dir:b16a9c313f3af0eb3267e3bc2402f75680aa3772d0955b6fb602a980dd47c434 in C:\mongodb 
# Tue, 09 Dec 2025 21:16:30 GMT
RUN mongod --version
# Tue, 09 Dec 2025 21:16:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Dec 2025 21:16:31 GMT
EXPOSE 27017
# Tue, 09 Dec 2025 21:16:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba0a59cfa716ac246ee7720bae9dc8d8daccce59539b2690c359e7e9f0f807b`  
		Last Modified: Tue, 09 Dec 2025 21:17:41 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d659d7082744b606b08ab445749097cb2ceae34ef06e080e55185e42a1ca91d`  
		Last Modified: Tue, 09 Dec 2025 21:17:41 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116870cde963b126e926f22df114e7a9c031f71acad11c7d383045df99d267aa`  
		Last Modified: Tue, 09 Dec 2025 21:17:42 GMT  
		Size: 76.8 KB (76810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba19bb436309ed968011b600d397f3edb4a0bb127c0e991c1efc4426cacd00a`  
		Last Modified: Tue, 09 Dec 2025 21:17:41 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a77bfe73e1835b37f902306192f3a2c8782d8844c86494b5feae91bb2cc5c8`  
		Last Modified: Tue, 09 Dec 2025 21:17:42 GMT  
		Size: 275.2 KB (275207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5d06fe3ac452126e1a47df068fde866f31653a53961f181bef90a0d86b1305`  
		Last Modified: Tue, 09 Dec 2025 21:17:41 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b29f6919b0b53982348391cf10f2f504dd2fccedb0b23a7272351c8fd61cc79`  
		Last Modified: Tue, 09 Dec 2025 21:17:56 GMT  
		Size: 617.1 MB (617119810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94792bfb82339eb9d0a2cde506e9403e73d0b9bc1a7be04fef01bc26d8f3197`  
		Last Modified: Tue, 09 Dec 2025 21:17:41 GMT  
		Size: 88.5 KB (88496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6f7610bf2d01592939d34b70f692344c6406dff026895c994c3b270d7e2d3a`  
		Last Modified: Tue, 09 Dec 2025 21:17:41 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc25c3f2c4c8bccc668bd662dbd5ad8db3bc57d81e57990ac95c7e7a7940986`  
		Last Modified: Tue, 09 Dec 2025 21:17:42 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459aef6c821c61d4f975cf210d278748b99155e67c959f2ea8512b5843b33b95`  
		Last Modified: Tue, 09 Dec 2025 21:17:41 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
