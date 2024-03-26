import socket
def get_ip_address(url):
try:
ip_address = socket.gethostbyname(url)
return ip_address
except socket.gaierror:
return None
# Example usage
website_url = input("Enter the website name :-")
ip_address = get_ip_address(website_url)
if ip_address:
print(f"The IP address of {website_url} is {ip_address}")
else:
print(f"Failed to retrieve the IP address of {website_url}")
