<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Cost Manager</title>
</head>
<body>
    <h1>Cost Manager</h1>
    <form action="cost-manager" method="post">
        <label>Enter User ID:</label>
        <input type="text" name="user_id">
        <br>
        <label>Enter First Name:</label>
        <input type="text" name="first_name">
        <br>
        <label>Enter Last Name:</label>
        <input type="text" name="last_name">
        <br>
        <label>Enter Category:</label>
        <input type="text" name="category">
        <br>
        <label>Enter the cost:</label>
        <input type="text" name="sum">
        <br>
        <input type="submit" value="Submit">
    </form>
    <%
        String userId = request.getParameter("user_id");
        String firstName = request.getParameter("first_name");
        String lastName = request.getParameter("last_name");
        String category = request.getParameter("category");
        String cost = request.getParameter("sum");
        if (cost != null) {
            double costValue = Double.parseDouble(cost);
            double vat = costValue * 0.2;
            double totalCost = costValue + vat;
    %>
    <button id="showCostBtn">Show Cost Details</button>
    <div id="costDetails" style="display: none;">
        <p>User ID: <%= userId %></p>
        <p>First Name: <%= firstName %></p>
        <p>Last Name: <%= lastName %></p>
        <p>Category: <%= category %></p>
        <p>Cost: $<%= cost %></p>
        <p>VAT: $<%= vat %></p>
        <p>Total Cost: $<%= totalCost %></p>
    </div>
    <%
        }
    %>
    <script>
        document.getElementById("showCostBtn").addEventListener("click", function() {
            document.getElementById("costDetails").style.display = "block";
        });
    </script>
</body>
</html>
