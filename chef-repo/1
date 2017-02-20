apt_update 'Updating the server and then install Apache' do
	frequency 86_400
	action :periodic
end

package 'apache2'

service 'apache2' do
supports :status => true
action [:enable, :start]
end

file '/var/www/html/index.html' do
	action :create
	content '<html> 
			<body><h1>Welcome to WebServer Apache</h1></body>
		</html>'
end
